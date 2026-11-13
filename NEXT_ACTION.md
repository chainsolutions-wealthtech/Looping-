# NEXT_ACTION — Point de reprise unique

```text
NEXT_ACTION = SPECIFY_DOCUMENT_CONSTITUTION_WORKFLOW
STATE = READY
```

## Action
Définir le contrat W1 de constitution et coordination documentaire à partir de la baseline qualifiée, des sources et des autorités existantes. Travail documentaire uniquement : connaître le squelette attendu, comparer l’existant, attribuer un propriétaire à chaque information, inscrire les relations entre documents et registres, définir leurs entrées/sorties et leur reprise.

## Entrées et prérequis
- Lire PROJECT_CONTEXT, STATUS, BASELINE, SOURCE_QUALIFICATION, WORK_METHOD, REQUESTS et la correspondance des workflows.
- Baseline capturée avec défauts connus selon ADR-0003 ; ne pas la présenter comme une CI verte.
- Utiliser WORK-SPEC-W1-001 dans le registre natif ; aucun claim ou droit n’est transféré par cette référence.
- Réobserver HEAD et permissions, puis réconcilier toute modification avant écriture.

## Done when
- cas dépôt nouveau et projet existant décrits séparément ;
- fichiers obligatoires, conditionnels, modèles, autorités et adaptateurs distingués ;
- responsabilités, hiérarchie, relations de coordination et rattachements aux registres explicites ;
- entrées, prérequis, étapes, sorties, erreurs, retours et critères de reprise observables ;
- méthode de création/réutilisation sans perte et contrôle d’intégrité définis ;
- demandes et critères de validation reliés au contrat, avec état SPECIFIED tant qu’il n’est pas implémenté ;
- mémoire, preuves et prochaine action mises à jour sans seconde queue.

## Limites
Cette action ne répare pas les workflows GSCC/GACR, n’active pas le moteur et ne déploie rien. Les défauts CI restent ouverts et le critère GREEN de LOOP-INIT-001 reste insatisfait.
