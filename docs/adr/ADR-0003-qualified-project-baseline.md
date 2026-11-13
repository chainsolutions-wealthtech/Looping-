# ADR-0003 — Baseline qualifiée et passage documentaire à W1

- Date d’enregistrement : 2026-11-13T07:47:09+00:00.
- Statut : ACCEPTED pour la qualification et les reports explicites du lot de découverte.
- Autorisation : U11 reprend l’action globale ; U08/U10 définissent le périmètre documentaire ; porte B sélectionnée par U09 et observée sur GitHub.
- Entrée observée : `e8fed08594726e3506bd1903877a5815ad68da9b` ; commit de capture de l’instruction : `6895981eade110765e518e9dac65499cc7456156`.

## Décision et portée
La tâche WORK-DISCOVER-001 consiste à capturer et qualifier l’état du projet, y compris ses limites. Ses critères sont satisfaits par la qualification des sources, l’inventaire Git complet, la baseline CI, le contexte/architecture et les registres initiaux de risques, dépendances et acceptation. Sa résolution est BASELINE_CAPTURED_WITH_KNOWN_DEFECTS ; elle ne signifie pas CI corrigée ou produit prêt.

Le choix du profil applicatif est explicitement différé jusqu’aux besoins et contrats de conception. L’enum valide DISCOVERY_REQUIRED et selected_profile=null sont conservés, avec une disposition de report explicite ; le candidat full-stack reste PLANNED. Le stockage documentaire Git/JSON actuel ne sélectionne pas à lui seul une stack applicative.

Serveur, domaine, répertoire et base serveur sont laissés non résolus avec justification : ce lot prépare des documents et le binding MCP du dépôt est UNCONFIGURED/NOT_RUN. Aucun runtime n’a été interrogé ni provisionné. Les outils MCP listés ne prouvent pas une connexion live ; aucune indisponibilité serveur n’est inventée. L’accès reste non vérifié, le transport préféré déclaré demeure DIRECT_MCP avec SSH en fallback.

L’action suivante est SPECIFY_DOCUMENT_CONSTITUTION_WORKFLOW, rattachée à WORK-SPEC-W1-001, documentaire uniquement. Elle précise d’abord le squelette, les responsabilités, les entrées/sorties, les dépendances et les modes nouveau dépôt/projet existant. Elle ne corrige pas la CI et ne déploie pas de moteur.

## Gates préservés
LOOP-INIT-001 reste IN_PROGRESS et son critère GREEN reste ouvert. Les défauts de portabilité CI-B01/CI-B02 restent ouverts. Une baseline avec défauts connus est une observation ; elle ne satisfait pas les gates de fonctionnement automatique, d’implémentation, de déploiement ou de production. Aucun gate n’est supprimé ou réétiqueté PASS.

Les états source-only du template ne sont pas restaurés. Le registre natif des travaux est réutilisé ; aucune queue, session GACR ou claim n’est créée par la porte B. READY signifie candidat documentaire sous ses contrôles propres, pas permission implicite.

## Projections
INTAKE-0003 est réconcilié comme TASK pour la poursuite demandée. Le changement du registre natif avance work_revision de 1 à 2. L’actualisation canonique de baseline/checkpoint avance canonical_revision de 3 à 4. Le curseur reflète ces révisions après réconciliation du lot. La mise à jour est une projection directe GitHub ; aucun résultat de helper CLI non exécuté n’est revendiqué.

## Preuves et reprise
docs/baseline/BASELINE.json et ses propriétaires détaillés portent les critères et limites. NEXT_ACTION, WORK-SPEC-W1-001, le pointeur mémoire et le checkpoint doivent rester alignés. La présence distante et les contrôles du lot sont vérifiés après publication ; le commit contenant un rapport n’invente jamais son propre SHA futur.
