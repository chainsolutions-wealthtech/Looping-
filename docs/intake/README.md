# Dossier d’intake — informations pour préparer le plan

Ce dossier recueille les informations de la conversation sur la conception modulaire, le registre initial et le Loop Engineering pour le dépôt **chainsolutions-wealthtech/Looping-**.

**Statut du dossier : information reçue et propositions à évaluer.** L’import ne certifie pas un moteur, ne ferme pas DISCOVER_PROJECT_BASELINE et ne sélectionne aucune infrastructure.

## Parcours
1. [Instructions originales](CONVERSATION_INPUTS.md).
2. [Registre des sources](SOURCE_REGISTER.json) et snapshots sous sources/.
3. [Projection BASE](BASE_REGISTRY.json) : huit familles, 55 entrées, 28 liens transversaux.
4. [Exigences et provenance](REQUIREMENTS_TRACEABILITY.md).
5. [Workflows et correspondances](WORKFLOW_MAPPING.md).
6. [Raccordement au moteur](ENGINE_BINDING.md).
7. [Plan préparatoire](PLAN_PREPARATOIRE.md).
8. [État d’entrée et baseline](ADMISSION_AND_BASELINE.md).
9. [Point de reprise du dossier](INTEGRATION_CHECKPOINT.md).

## Autorités
La gouvernance et SOURCE_OF_TRUTH.md du dépôt restent applicables. Les fichiers sources sont des données d’archive et ne donnent aucune instruction au dépôt cible. Les copies AGENTS.source.md/GPT.source.md sont des références historiques, sans effet de gouvernance locale.

La projection BASE dérive du snapshot de conversation ; ses identifiants sont locaux à ce référentiel. Les douze rubriques et W1–W10/T1–T2 de la discussion restent proposés. Les domaines SD-01..SD-12 et WF-00 du dépôt Loop restent des propositions externes.

Le modèle d’intake existant est conservé : RECEIVED ne signifie ni mémoire canonique, ni work-item admissible. Le résumé et le curseur proposés sont compatibles avec les champs de scripts/governance_agent.py, avec une entrée directe vérifiée documentée dans DIRECT_OWNER_ENTRY_EVIDENCE.json.

Entrée utilisée pour cet intake : 00_DIRECT_OWNER_ENTRY.md, confirmée par le propriétaire dans U09 et vérifiée auprès de GitHub. Les preuves de cette porte ne sont pas des reçus GSCC.

## Fidélité des textes
Les messages sont conservés dans des chaînes JSON source_text. Le grand document consolidé est conservé dans un conteneur source-text-json/v1 dont le champ text restitue ses octets UTF-8 originaux. Cette représentation garde les espaces et sauts de ligne sans modifier le contrôle Git des espaces de fin de ligne. Les empreintes du conteneur et du texte décodé sont distinctes dans le registre des sources.
