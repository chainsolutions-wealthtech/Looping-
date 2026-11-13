# Point de reprise du dossier d’information

> Intake documentaire reçu ; les propositions restent à évaluer selon les autorités existantes.

STATE = RECONCILED_WITH_OPEN_DESIGN_QUESTIONS
TARGET = chainsolutions-wealthtech/Looping-
BASELINE_INPUT_HEAD = 86f0317905eb1eaf790e4f2f58a7e3e41735c2bf
INTAKE = INTAKE-0001
GLOBAL_NEXT_ACTION_REF = NEXT_ACTION.md

## Contenu intégré
Sources, instructions originales, projection BASE, traçabilité, correspondance des workflows, contrat moteur et plan préparatoire. Le curseur conserve canonical_revision=0 et work_revision=0.

## Limites
Le dossier n’installe pas de moteur et ne ferme pas DISCOVER_PROJECT_BASELINE. Les propositions ne deviennent pas canoniques automatiquement. Aucun nouveau work-item ou claim n’est attribué.

## Reprise
Lire le registre des sources, les instructions et PLAN_PREPARATOIRE.md, puis évaluer l’intake avec le mécanisme existant. Une contradiction reste HOLD_FOR_REVIEW pour son périmètre. Mettre à jour les propriétaires existants uniquement selon une disposition autorisée.

## Entrée et autorisation
La porte B 00_DIRECT_OWNER_ENTRY.md a été confirmée par U09 et vérifiée avec les faits GitHub natifs. Voir DIRECT_OWNER_ENTRY_EVIDENCE.json. La route A n’a pas de release attestée ; elle reste distincte. L’écriture est gardée par le HEAD de référence, sans force-push.

## Application et vérification
- Commit d’import : `217f2380d19dc9b67eb60aef848c42ae7171062f`.
- Les 30 blobs de l’import ont été vérifiés et sept contenus principaux relus.
- Voir [VERIFICATION.md](VERIFICATION.md) pour les contrôles et les résultats des six exécutions GitHub Actions.
- La validation de structure a réussi ; la CI complète reste en échec sur des chemins absents dès la baseline (migration SQL first-touch et registre de namespace). Les journaux attestent les points d’arrêt ; les étapes suivantes ne sont pas réputées validées.


## Revue ultérieure
La disposition courante d’INTAKE-0001 est RECONCILED / MEMORY, décidée dans ADR-0002 après U10. La reprise active est [docs/memory/CHECKPOINT.json](../memory/CHECKPOINT.json). La conservation des sources et la qualification des propositions n’installent pas le moteur et ne ferment pas la baseline métier. Ce fichier conserve les preuves d’import ; il n’est plus le propriétaire de l’action globale.
