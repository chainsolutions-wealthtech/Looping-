# Méthode de travail de Looping-

Statut : méthode documentaire définie à partir de U01..U10 et de la gouvernance existante. Son automatisation complète reste à développer. La porte B a été choisie explicitement ; l’intention courante est CONTEXT_INTAKE / PLANNER_AGENT pour la mémoire et la planification, sans autorité d’exécution serveur.

## Fil conducteur
Constituer les sources et le registre initial avant de fixer l’architecture applicative. Chaque information doit être retrouvable, qualifiée et reliée à un résultat. Le registre BASE reste dans ses huit parties. Les versions historiques, propositions, décisions du propriétaire, artefacts implémentés et preuves d’exécution sont distingués.

## Deux situations d’entrée
Pour un dépôt nouveau : inventorier le squelette existant, constituer les propriétaires documentaires manquants, enregistrer les intentions, concevoir et planifier avant le code. Pour un projet existant : lire et inventorier documents, mémoire, code, interfaces, données et travaux ; réconcilier les écarts avant toute extension. Dans les deux cas, réutiliser les mécanismes présents et préserver les preuves.

## Boucle de traitement d’une instruction

| Étape | Entrée | Action et propriétaire | Sortie vérifiable |
|---|---|---|---|
| 0 — Arriver | Dépôt et mission explicites | Satisfaire la porte choisie ; observer acteur, droits, branche et HEAD | Preuves natives d’entrée, sans session inventée |
| 1 — Capturer | Message ou document accessible | Conserver le texte exact, provenance, ordre connu, empreinte ; horodatage inconnu à null | Source et entrée du ledger |
| 2 — Enregistrer | Source capturée | Ajouter l’intake natif RECEIVED ; ne pas confondre avec décision ou work-item | ID d’intake et curseur monotone |
| 3 — Qualifier | Intake et autorités actuelles | Distinguer demande, décision, proposition, doublon, constat, contradiction ; évaluer la provenance | Revue motivée, effet canonique/work explicite ; contradiction en HOLD_FOR_REVIEW |
| 4 — Rattacher | Information qualifiée | Relier source, demande, BASE, composant, document responsable et phase | Références résolues sans propriétaire concurrent |
| 5 — Concevoir | Besoin et informations manquantes | Définir règles métier, données, interactions, entrées/sorties et critères ; conserver les inconnues | Cahier des charges et contrats évolutifs à qualifier |
| 6 — Planifier | Conception suffisamment définie | Ordonnancer les lots selon dépendances et preuves de sortie ; tenir REQUESTS et ROADMAP | Plan explicite, distinct de la file exécutable |
| 7 — Réaliser | Lot admis et autorisations réelles | Utiliser le registre de travaux existant si cette route est choisie ; respecter permissions, claims, HEAD et collisions | Artefacts bornés ; aucune autorité déduite du seul registre |
| 8 — Vérifier | Artefacts et baseline | Contrôles adaptés, empreintes, références, fidélité des sources, non-régression ; distinguer défaut hérité et défaut introduit | Résultats, écarts, runs et limites documentés |
| 9 — Publier et reprendre | Lot vérifié dans son périmètre | Commit sans force avec expected_sha ; relecture distante ; mettre à jour mémoire et checkpoint | Preuve GitHub et prochaine action globale unique |

## Relations et impacts
Une source alimente une ou plusieurs demandes. Une demande peut être détaillée en plusieurs résultats. Une décision qualifie un choix ; elle n’efface pas la source. Une modification oblige à examiner les demandes dépendantes, les documents responsables, la conception, les critères, la roadmap et les preuves. Un lien BASE « mobilise » ou « associe » ne devient pas silencieusement une dépendance de code.

Une contradiction est enregistrée avec les deux sources et maintenue en revue pour son périmètre. Les travaux indépendants restent possibles dans leurs autorisations. Une information manquante reste une question ouverte ; elle n’est pas remplacée par une valeur supposée.

## Organisation et règles d’écriture
GitHub est la surface persistante ; le scratch sert à préparer et contrôler. Les JSON portent les registres structurés ; les documents de contexte, état, méthode, architecture, roadmap et ADR ont chacun leur responsabilité. TODO pointe vers le registre détaillé. Aucun agent ne crée une seconde queue ou copie l’état actif d’un autre projet.

Les identifiants de demandes et de sources sont locaux au dépôt. Les identifiants fournisseur, liveness, sessions, serveurs, répertoires, déploiements et résultats live exigent leurs propres observations. Les credentials restent hors du dépôt. Le travail historique sur MCP n’autorise pas à modifier MCP.

## Mise à jour de la mémoire
À chaque changement durable : conserver la source ; actualiser son propriétaire détaillé ; modifier les index seulement si le routage ou l’état global change ; ajouter les preuves matérielles à ACTIONS/WORK_LOG ; mettre à jour le checkpoint. Une ancienne réponse peut être corrigée par une qualification datée sans réécrire son texte source. La mémoire décrit la vérité actuelle et renvoie à l’archive pour la chronologie.

## Limite de la présente méthode
La capture et la réconciliation documentées sont réalisées par l’agent dans la session active. Un collecteur automatique de toutes les conversations, un classement autonome, le chargeur BASE et l’exécution de toutes les boucles ne sont pas démontrés par ces fichiers. Leur conception puis leur validation figurent dans la roadmap.
