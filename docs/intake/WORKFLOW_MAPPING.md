# Correspondance des workflows — proposition

Le référentiel initial BASE demeure organisé selon les huit parties de la source. Les workflows de la discussion sont des candidats, pas des workflows actifs du dépôt.

| Repère proposé | Objet | Relations BASE à examiner |
|---|---|---|
| W1 | Constitution et coordination documentaire | Couverture et propriétaires de toutes les familles ; préparation des registres |
| W2 | Arrivée, audit et réconciliation | Contexte, état, sources et gouvernance existante |
| W3 | Collecte et qualification | Nature de l’information, provenance et rattachements BASE |
| W4 | Cahier des charges évolutif | Besoins concrets du projet et critères, liés aux repères BASE |
| W5 | Software Design / architecture | BASE-01..05, BASE-06-01..02, BASE-07 et BASE-08 |
| W6 | Arbitrage et planification | Dépendances et résultats issus de la conception |
| W7 | Réalisation | Périmètre autorisé ; options effectivement retenues |
| W8 | Vérification et non-régression | BASE-06-04, exigences et preuves |
| W9 | Livraison et observation | BASE-06-03, BASE-07-03, autorisations réelles |
| W10 | Analyse d’impact | Changements sur sources, besoins, modèles, travaux et preuves |
| T1 | Mémoire et continuité | Résultats, questions, état et reprise |
| T2 | Intégrité et traçabilité | Identifiants, versions, références et propriétaires |

## Réutilisation obligatoire de l’existant à étudier
Looping- possède déjà un modèle d’intake, des intentions de connexion, des entrées, des sessions/claims, des checkpoints et une gouvernance. Ces mécanismes ne doivent pas être remplacés par une seconde file ou un second dispatcher.

Les cinq boucles spécialisées retrouvées dans la source MCP (migration, nettoyage, documentation, tests, architecture) et les dix phases de sa boucle standard sont des éléments historiques distincts du catalogue candidat ci-dessus.

WF-00 du dépôt Loop est une spécification candidate externe ; une correspondance de rôle peut être étudiée avec W1, sans les fusionner ni transférer automatiquement leur autorité.
