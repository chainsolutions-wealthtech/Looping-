# Compatibilité CI du dépôt client — diagnostic de baseline

Audit au commit `e8fed08594726e3506bd1903877a5815ad68da9b`. Ce document possède le détail du diagnostic ; le statut global et les runs sont indexés dans BASELINE.json. Les journaux natifs ont été relus. Aucun correctif de code ou workflow n’est appliqué par ce rapport.

## Frontière source/client attestée
`.governance/control-plane-policy.json` déclare `current_role=GOVERNED_TARGET_CLIENT` et classe `docs/control-plane`, `.governance/control-plane-state` et `.governance/control-plane-db` parmi les source_only_paths. `scripts/initialize_governance.py`, lignes 221–226 au SHA d’audit, supprime ces chemins lors de l’initialisation. L’arbre Git complet confirme leur absence et celle de `.template-source`.

Cette absence est conforme à la frontière de distribution. La validation de structure du client réussit. Le défaut apparaît lorsqu’un autre chemin exécutable suppose encore les données réservées au dépôt modèle.

## CI-B01 — Dépendance first-touch non portable
- Preuves : Governance CI [43385471798](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43385471798), job 131752790083 ; Observable Arrival [43385471771](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43385471771), job 131752790660.
- Le workflow Governance CI lance sans condition `scripts/test_first_touch_field_block_gate.py`. Le test appelle build_capture_database, qui appelle install_schema.
- `scripts/first_touch_field_block_gate.py`, lignes 45–47, lit `.governance/control-plane-db/007_first_touch_field_block_gate.sql`. Le workflow Observable Arrival appelle également le même constructeur sans matériel portable distinct.
- Les deux journaux se terminent par FileNotFoundError sur cette migration, déjà absente à la baseline.
- Le catalogue lu ensuite par ce constructeur dépend également du modèle de fichiers ; les erreurs ultérieures ne sont pas présumées validées.

Correctif à concevoir : isoler le schéma et les catalogues génériques nécessaires aux clients, garder séparés états et seeds propres au dépôt source, puis distribuer les dépendances portables par le mécanisme de versionnement existant. Ajouter des fixtures source/client et démontrer le parcours client. Copier seulement la migration 007 ou ignorer l’ensemble des tests ne démontre pas cette portabilité.

## CI-B02 — Assertion de namespace réservée au source appelée par un test client
- Preuve : Continuity Relay [43385471692](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43385471692), job 131752789893, étape Validate GACR state.
- Cette étape exécute `scripts/test_gscc_issue_control_bridge.py` après les tests de coordination et de bus.
- Le traceback désigne précisément `test_control_dispatch_id_is_registered_canonical_namespace`, lignes 363–375 ; la ligne 368 lit `.governance/control-plane-state/namespace-work-registry.json` sans garde source/client.
- Le point d’arrêt n’est donc pas un appel direct à `validate_namespace_work_registry.py` par ce workflow : il est dans cette assertion du test GSCC.
- Governance CI possède déjà une garde `.template-source` autour de son étape directe de validation du namespace, mais cette garde ne protège pas l’assertion appelée par le workflow de relais.

Correctif à concevoir : distinguer l’assertion d’intégrité du catalogue source de la validation du contrat portable de dispatch client ; conserver les deux garanties avec des fixtures adaptées. Aucune seconde autorité de namespace ni copie de l’historique source n’est installée ici.

## Surface à examiner avant une correction
Les lecteurs des migrations, catalogues, projections source-only, tests de fixtures et workflows d’entrée doivent être inventoriés ensemble. Les autres références absentes sont des dépendances statiques à examiner, pas des erreurs d’exécution supplémentaires déclarées comme observées. Un correctif générique doit être traçable au fournisseur du template et à sa distribution vers le client ; ce lot n’écrit dans aucun autre dépôt.

## Contrat de validation du futur correctif
1. Le bootstrap client conserve la suppression des états privés/source-only.
2. Les tests génériques s’exécutent dans une fixture client propre et dans une fixture source distincte.
3. La matérialisation first-touch requise par le client reçoit toutes ses dépendances génériques.
4. Les contrats de namespace et de dispatch restent vérifiés selon leur propriétaire.
5. Les parcours d’entrée A et B, les états existants, les sources et les projections propres au client sont préservés.
6. La CI est exécutée au SHA exact ; les tests suivants ne sont déclarés validés qu’après leur exécution réelle.

## Disposition de découverte
La capture de baseline est qualifiée avec ces défauts ouverts. La rédaction du contrat W1 peut avancer sur des documents versionnés avec la porte B vérifiée. L’activation du parcours A, du relais automatisé, du moteur et la clôture GREEN de LOOP-INIT-001 restent non acquises. Aucun reçu de release ou état live n’est fabriqué.
