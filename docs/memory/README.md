# Mémoire canonique de Looping-

Le dépôt GitHub est la surface persistante. La mémoire est un ensemble de propriétaires reliés par le pointeur existant [.governance/canonical-memory/current.json](../../.governance/canonical-memory/current.json), sous la hiérarchie de [SOURCE_OF_TRUTH.md](../../SOURCE_OF_TRUTH.md). Ce fichier est une carte de lecture, pas une seconde mémoire d’état.

| Information recherchée | Propriétaire détaillé |
|---|---|
| Identité, mission, périmètre et contexte | [PROJECT_CONTEXT.md](../../PROJECT_CONTEXT.md) |
| État courant et limites de vérification | [STATUS.md](../../STATUS.md) |
| Textes utilisateur U01..U09 | [CONVERSATION_INPUTS.md](../intake/CONVERSATION_INPUTS.md) |
| Nouvelle instruction exacte U10 | [sources/U10.json](sources/U10.json) |
| Index des échanges, empreintes et lacunes | [CONVERSATION_LEDGER.json](CONVERSATION_LEDGER.json) |
| Sources historiques et snapshots | [SOURCE_REGISTER.json](../intake/SOURCE_REGISTER.json) |
| Référentiel initial en huit parties | [BASE_REGISTRY.json](../intake/BASE_REGISTRY.json) |
| Demandes, contextes, dépendances, critères et restant | [REQUESTS.json](REQUESTS.json) |
| Méthode de travail | [WORK_METHOD.md](../WORK_METHOD.md) |
| Architecture actuelle et cible | [ARCHITECTURE.md](../ARCHITECTURE.md) |
| Phases, sorties et dépendances | [ROADMAP.md](../../ROADMAP.md) |
| Décisions | [DECISIONS.md](../DECISIONS.md) et ADR associés |
| Actions matérielles et preuves | [ACTIONS.json](ACTIONS.json) ; historique humain dans SUIVI/WORK_LOG |
| Reprise globale | [NEXT_ACTION.md](../../NEXT_ACTION.md), puis [CHECKPOINT.json](CHECKPOINT.json) |
| Travaux exécutables et claims | [.governance/work/](../../.governance/work/) ; aucune seconde file |

## Conservation et qualification
Les textes sources restent conservés intégralement chez leur propriétaire et sont référencés par empreinte. Un ancien état reste une preuve historique ; l’état courant est lu dans STATUS et le pointeur, pas déduit d’une ancienne réponse. Les propositions W1–W10/T1–T2 et le raccordement moteur restent des conceptions à qualifier. L’acceptation de l’archive ne vaut pas activation de son contenu.

Les lacunes de capture sont explicites dans le ledger. Il ne s’agit pas d’un export natif exhaustif du fournisseur. Aucun horodatage de message ou identifiant privé n’est inventé. Les futures écritures sont effectuées par les agents au cours du travail ; aucun service permanent de collecte n’est installé.

## Reprise
Après validation de la porte d’entrée choisie : lire PROJECT_CONTEXT, STATUS, le pointeur mémoire, CHECKPOINT, les demandes concernées, la méthode et la phase de roadmap correspondante. Réobserver le HEAD en ligne et réconcilier tout mouvement avant écriture. Les références externes à MCP et Loop sont des sources ; elles ne transfèrent ni gouvernance ni autorité à Looping-.

## Route de découverte
La baseline qualifiée et ses limites ont pour propriétaire [docs/baseline/BASELINE.json](../baseline/BASELINE.json), avec inventaire, qualification et diagnostic reliés depuis son [index](../baseline/README.md). L’action globale se lit dans NEXT_ACTION ; la découverte achevée ne clôt pas le gate CI.
