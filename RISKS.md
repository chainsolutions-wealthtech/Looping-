# RISKS — Risques et écarts initiaux de Looping-

| ID | Risque ou écart | Impact | Probabilité / observation | Mesure | Statut |
|---|---|---|---|---|---|
| R-INIT-001 | Contexte projet non initialisé | Ancien risque du template | Contexte désormais renseigné et versionné | PROJECT_CONTEXT et ADR-0002 | CLOSED — contexte documenté |
| R-BASE-001 | Dépendances source-only encore appelées dans le client | Bloque la CI complète et des chemins d’arrivée/continuité | Échec observé ; probabilité statistique non estimée | Diagnostic CI_COMPATIBILITY ; correctif portable à concevoir et vérifier | OPEN |
| R-BASE-002 | Prendre une source ou une spécification pour une capacité active | Mauvais choix de travaux ou faux état opérationnel | Risque de conception ; non chiffré | Qualifier sources, exigences, décisions, preuves et états | OPEN — contrôles documentaires présents |
| R-BASE-003 | Historique brut incomplet | Perte d’une condition ou d’un choix ancien | Lacunes exposées dans le ledger | Compléter uniquement avec des sources accessibles et datables | OPEN |
| R-BASE-004 | Profil ou infrastructure choisis prématurément | Dépendances et coûts sans besoins établis | Pas d’activation observée | Report explicite dans ADR-0003 et projections | DEFERRED |
| R-BASE-005 | Mouvement concurrent du HEAD | Écrasement ou revue d’un état périmé | Possible ; non chiffré | expected_sha, comparaison des arbres et réconciliation | CONTROLLED_PER_WRITE |
| R-BASE-006 | Propriétaires ou registres concurrents | Divergence de mémoire et de planning | Risque architectural | Pointeur unique, propriétaires détaillés, registre natif réutilisé | OPEN — contrôle requis |

Les défauts observés et leur causalité sont possédés par docs/baseline/CI_COMPATIBILITY.md ; cette table décrit leurs impacts et mesures. Aucune probabilité quantitative ni gravité réglementaire n’est inventée.
