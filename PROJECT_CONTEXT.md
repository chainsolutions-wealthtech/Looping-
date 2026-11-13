# PROJECT_CONTEXT

- Repository: `chainsolutions-wealthtech/Looping-`
- Project: `Looping-`
- Project type: `generic`
- Owner: `@chainsolutions-wealthtech`
- Canonical branch: `main`
- Initialized at: `2026-11-13T05:56:34+00:00`

## Mission
Concevoir progressivement un système Loop Engineering réutilisable, modulaire et gouverné. Il doit recevoir des informations, préserver leur provenance, constituer un cahier des charges évolutif, organiser les documents, préparer l’architecture et la planification, puis permettre des cycles d’exécution, de vérification et de reprise fondés sur des preuves.

## Origine et fil rouge
U01 et U06 désignent la base de conception en huit parties ; U02/U05 imposent étapes et registre initial ; U03 demande les workflows ; U04 demande la reconstitution historique de MCP ; U07 demande le rattachement au moteur ; U08 désigne ce dépôt pour intégrer les informations et préparer le plan ; U09 sélectionne l’entrée directe ; U10 demande mémoire canonique, registre des demandes, contexte, méthode, architecture et roadmap. Les textes sont routés par docs/memory/CONVERSATION_LEDGER.json.

## Scope

### In scope
- Conserver les informations projet accessibles, leurs sources, versions et limites.
- Construire le registre initial BASE, la mémoire et le registre des demandes.
- Préparer la constitution/coordination documentaire, les workflows, le cahier des charges, les contrats de raccordement, l’architecture et le plan.
- Réutiliser le modèle d’intake et la gouvernance déjà présents ; préserver les mécanismes existants.
- Décrire séparément un dépôt nouveau et la reprise d’un projet existant.

### Out of scope for this documentary increment
- Déployer une application ou provisionner serveur, domaine, base, broker ou cluster.
- Modifier Patricked-code/MCP ou chainsolutions-wealthtech/Loop.
- Assimiler la conservation d’un document à l’activation de tous les mécanismes qu’il décrit.
- Installer une seconde Task Queue, un second dispatcher ou un collecteur caché de conversations.

## Architecture / stack
Architecture documentaire actuelle : Git, sources archivées, JSON, autorités Markdown et scripts Python de gouvernance hérités du template. Architecture fonctionnelle cible : docs/ARCHITECTURE.md. Le prototype loop.py est une source archivée, pas le moteur installé de Looping-.

Technical intent is tracked separately in `.governance/project-profile.json`. A planned profile is not evidence of implementation. Le profil reste DISCOVERY_REQUIRED ; aucun choix Node.js/Next.js/PostgreSQL n’est activé par ce lot. Les technologies de BASE sont des références à qualifier par projet.

## Infrastructure / deployment
See `.governance/infrastructure-intent.json`. Serveur, domaine, répertoire et base serveur restent non résolus. Aucun accès runtime n’est attesté par ce travail GitHub. Le transport préféré déclaré est DIRECT_MCP, avec SSH en fallback ; cela ne prouve pas leur disponibilité.

## External systems
GitHub est observé au moyen du connecteur authentifié. Les snapshots MCP et Loop sont des références externes avec provenance. Leur présence n’établit ni connexion live ni transfert d’autorité. MCP comme projet logiciel et MCP comme outil d’exécution restent deux contextes distincts.

## Critical constraints
Respecter GOVERNANCE, SOURCE_OF_TRUTH et la non-régression ; conserver chronologie et sources ; ne pas inventer de dates, capacités, identités ou validations ; garder une prochaine action globale ; suivre les dépendances ; enregistrer les contradictions et les inconnues. Les détails de travail sont dans docs/WORK_METHOD.md ; les demandes sont dans docs/memory/REQUESTS.json.

## Disposition de découverte
ADR-0003 qualifie la baseline de ce dépôt avec défauts connus. Le profil applicatif reste volontairement en découverte et ses choix sont différés ; l’infrastructure et l’accès runtime restent non résolus, sans appel serveur. Le détail des observations, limites et prérequis W1 se lit dans docs/baseline/BASELINE.json. Ce report est une décision de portée documentaire, pas un constat d’absence physique des ressources.
