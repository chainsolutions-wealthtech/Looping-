# ROADMAP — Construction progressive de Looping-

Cette roadmap ordonne les demandes de docs/memory/REQUESTS.json. Elle constitue le plan documentaire courant ; elle n’est ni une queue exécutable ni une activation automatique de tous les lots. L’action globale unique reste dans NEXT_ACTION.md. Les phases du plan préparatoire importé conservent leur provenance ; la présente roadmap est leur déclinaison pour ce dépôt.

| Phase | État actuel | Dépendances | Résultat et livrables | Condition de sortie |
|---|---|---|---|---|
| RP-00 — Sources et chronologie | Corpus accessible enregistré ; lacunes ouvertes | Aucune | U01..U10, sources historiques, ledger et preuves d’import ; REQ-005/009/011 | Sources accessibles vérifiées ; couverture et lacunes explicites ; reconstitution exhaustive non prétendue |
| RP-01 — Mémoire et registre | DOCUMENTED et relu sur GitHub ; preuves dans le checkpoint | RP-00 | Mémoire canonique, 20 demandes, méthode, contexte, architecture initiale, roadmap ; REQ-001/002/006/010/012..020 | Propriétaires uniques, sources exactes, références cohérentes, intake revu et relecture GitHub |
| RP-02 — Baseline et qualification | IN_PROGRESS ; CI complète bloquée | RP-01 | Baseline code/docs/CI, frontière source/client, écarts et décisions de qualification ; REQ-005, FIND-001 | Défauts hérités caractérisés, stratégie de correction admise, profil et infrastructure observés ou explicitement différés ; aucune fausse CI verte |
| RP-03 — Constitution documentaire et workflows | PLANNED | RP-02 | Contrat W1 en premier : squelette, fichiers présents/manquants, propriétaires, entrées/sorties et reprise ; puis correspondances W2..W10/T1..T2 ; REQ-003/004 | Parcours dépôt nouveau/existant définis, prérequis et sorties vérifiables, aucun dispatcher doublonné |
| RP-04 — Cahier des charges et architecture cible | Initialisation documentaire faite ; détail PLANNED | RP-03 | Besoins, règles métier, données, qualité, profils d’application de BASE, contrats d’intégration ; REQ-008/019 | Informations manquantes et décisions ouvertes visibles ; conception suffisante pour le lot concerné |
| RP-05 — Contrat moteur et premier raccordement | SPECIFIED_NOT_IMPLEMENTED | RP-04 | Schéma/version BASE, chargeur, rattachements, compatibilité du prototype et ports existants ; REQ-007/008 | Scénarios de validation définis, lot borné admis, raccordement démontré avec ses limites |
| RP-06 — Boucle complète démontrée | PLANNED | RP-05 | Une instruction accessible → source → demande → document → plan → travail autorisé → preuve → reprise | Traçabilité bout en bout, ambiguïté/contradiction et interruption traitées ; non-régression démontrée |
| RP-07 — Produit applicatif et exploitation | PLANNED ; aucune infrastructure activée | RP-06 | Interface, API, persistance et déploiement selon besoins et décisions ultérieurs | Autorisations, environnement, tests, preuves de livraison et d’observation réels ; aucune déduction d’état |

## Ordre de travail et retours
La collecte reste ouverte pendant les phases suivantes : une nouvelle source reçoit un intake, puis une qualification et une analyse d’impact. Une contradiction renvoie vers la première décision ou sortie concernée ; elle ne réinitialise pas tout le projet. Un changement de besoin réévalue les dépendances avant de modifier le plan. Les statuts d’une phase ne remplacent pas ceux de chaque demande.

## Livrable à détailler en premier après la baseline
Le mécanisme W1 de constitution et coordination documentaire : connaître le squelette attendu ; comparer les fichiers présents ; distinguer autorités, registres, modèles et adaptateurs ; créer seulement le nécessaire ; inscrire relations et obligations ; vérifier l’intégrité ; laisser une reprise fiable. Les autres workflows sont reliés à ce sous-système après sa définition, sans perdre leurs sources historiques.

## Validation et disponibilité
La présence des documents ne signifie pas readiness du moteur ou du déploiement. Le lot documentaire est contrôlé par parsing JSON, fidélité des sources, intégrité des liens et comparaison du tree Git ; la CI hérite encore de points d’arrêt attestés. Le checkpoint doit porter les preuves de publication après relecture. Aucune date de livraison ni charge non évaluée n’est inventée.
