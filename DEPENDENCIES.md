# DEPENDENCIES — Dépendances initiales

| ID / dépendance | Type et propriétaire | Contrat / version observée | Criticité / panne | Alternative et preuve |
|---|---|---|---|---|
| DEP-01 GitHub Looping- | Source persistante ; propriétaire du dépôt | Branche main, repository_id 1456213061 ; HEAD épinglé dans BASELINE | Écriture native et disponibilité nécessaires à la publication | Garder une préparation locale ; aucune publication supposée ; ref et relecture natives |
| DEP-02 Gouvernance et template | Fournisseur Governed Repository Template ; règles locales prioritaires | Manifest observé 2.8.43 ; rôle client, source_only_paths | Défauts de distribution bloquent certaines validations | Correction compatible à qualifier ; CI_COMPATIBILITY possède le diagnostic |
| DEP-03 Sources et BASE | Sources utilisateur/historiques ; registre versionné | Huit familles, 55 entrées ; empreintes et SHA dans les propriétaires | Sans provenance, classement et conception non fiables | Conservation des textes et lacunes explicites ; SOURCE_REGISTER et ledger |
| DEP-04 Python et workflows hérités | Exécution de la gouvernance et tests en CI | Scripts Python présents ; versions effectives liées aux journaux de runs | Présence du code ne certifie pas tous les parcours | Contrôles documentaires natifs possibles ; ne pas certifier les tests SKIPPED |
| DEP-05 Bibliothèque plugin GSCC | Source d’adaptateur fournisseur | plugins/gscc-github-mcp avec Dockerfile, requirements et server.py | Construction/exécution non vérifiées pour Looping- | Référence de code seulement ; aucune connexion ou déploiement inféré |
| DEP-06 MCP et accès serveur | Intégration externe future | Binding du dépôt UNCONFIGURED / NOT_RUN | Nécessaire seulement aux futurs lots runtime autorisés | Différé pour le contrat W1 ; DIRECT_MCP préféré, SSH fallback déclaré mais non attesté |
| DEP-07 Besoins et contrats | Propriétaire du projet ; documents responsables | W1 et moteur BASE à spécifier ; profil applicatif non sélectionné | Bloque les choix d’implémentation définitifs | Avancer les contrats documentaires avec inconnues visibles |

Les credentials ne sont pas stockés ici. La déclaration d’un outil ou d’un profil ne prouve pas sa disponibilité live. Les dépendances de correction sont des travaux à préparer ; aucune opération sur un autre dépôt ou serveur n’est lancée par cet inventaire.
