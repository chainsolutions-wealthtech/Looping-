# ADR-0002 — Mémoire canonique et registre des demandes de Looping-

- Date : 2026-11-13 ; enregistrement durant la revue de U10.
- Statut : ACCEPTED pour le socle documentaire ; architecture applicative et automatisations futures restent PROPOSED.
- Sources : U08, U09, U10 ; GOVERNANCE et SOURCE_OF_TRUTH.

## Contexte
Le propriétaire demande de conserver les informations sur GitHub, dans une base ou un registre, puis de constituer mémoire canonique, demandes, contexte, méthode, architecture et roadmap. Le dépôt possède déjà un intake, un pointeur mémoire, des autorités documentaires et une file de travaux. Le premier import est prouvé, mais ses dispositions sont encore RECEIVED.

## Décision
Utiliser les JSON versionnés et les documents responsables dans ce dépôt comme registre persistant pour ce lot. Réutiliser le pointeur .governance/canonical-memory/current.json et sa hiérarchie ; ajouter des routes explicites vers les propriétaires. Le registre REQUESTS est un registre de demandes, pas une seconde Task Queue.

Conserver les sources exactes accessibles avec provenance et empreintes ; archiver les réponses disponibles et les preuves matérielles ; afficher les lacunes. Les horodatages inconnus restent null. Les propositions, décisions, états documentaires et preuves live ne sont pas confondus.

Réconcilier dans l’ordre INTAKE-0001 comme MEMORY (conservation et qualification du corpus) puis INTAKE-0002 comme DECISION (mandat documentaire explicite). Les effets canoniques concernent les propriétaires documentaires et les faits vérifiés ; ils n’adoptent pas automatiquement toutes les propositions des archives. Aucun effet work, nouveau claim, session, transport ou permission runtime n’est créé.

Le pointeur bootstrap observé avait canonical_revision=1 et work_revision=1 ; le curseur intake était à 0/0. Deux revues canoniques donnent 3/1 pour le pointeur et le curseur. Cette précision corrige la portée de la phrase historique A01 sur les révisions à zéro, sans modifier son texte source. Le checkpoint documentaire est une trace directe GitHub, pas une attestation de session GACR.

## Conséquences
Les informations sont lisibles, diffables et rattachables à Git sans base serveur supplémentaire. Une base SQL éventuelle exige ultérieurement un schéma, une décision et une stratégie de migration/projection. SOURCE_OF_TRUTH conserve sa priorité ; README, TODO et la mémoire servent de routes vers les propriétaires.

La baseline métier reste ouverte. Les défauts de portabilité client constatés en CI ne sont pas corrigés par cette décision. Les choix d’architecture distribuée, stack, hébergement, automatisation des workflows et déploiement ne sont pas activés par le présent ADR.
