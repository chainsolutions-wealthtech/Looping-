# Qualification des sources de la baseline

Référence de lecture : `e8fed08594726e3506bd1903877a5815ad68da9b`. Propriétaires des textes : docs/intake/CONVERSATION_INPUTS.md, docs/memory/sources/U10.json et U11.json ; index : docs/memory/CONVERSATION_LEDGER.json. Les empreintes et références historiques sont conservées dans les registres existants.

| Source | Nature retenue | Effet admis | Ce qui reste ouvert |
|---|---|---|---|
| U01 / U06 | Base désignée par le propriétaire | Référence de conception en huit parties et 55 entrées | Applicabilité des technologies à un projet particulier |
| U02 / U05 | Exigence d’ordre et de structure | Registre initial avant le détail du moteur ; étapes préparées | Contrat détaillé de constitution documentaire |
| U03 / U07 | Demande de workflows et raccordement | Besoin à spécifier ; propositions W1–W10/T1–T2 conservées | Automatisation, chargeur BASE, impact et orchestration non démontrés |
| U04 | Recherche historique | Exploiter les snapshots accessibles et leur provenance | Exhaustivité et anciens messages indisponibles |
| U08 / U10 | Mandat de constitution et de planification | Sources, mémoire, demandes, contexte, méthode, architecture et roadmap propres à Looping- | Implémentation applicative et déploiement hors de ce lot |
| U09 | Sélection de porte | Entrée B sur observations GitHub réelles de l’acteur, des droits et du HEAD | Aucun claim, session ou droit serveur déduit |
| U11 | Demande de reprise de l’action globale | Exécuter la découverte et enregistrer son résultat | La prochaine action doit conserver ses propres critères |
| Snapshots MCP | Références historiques à un SHA identifié | Comprendre l’organisation et les mécanismes retrouvés | Aucun transfert d’autorité, état courant MCP ou modification MCP |
| Snapshots Loop / prototype | Références externes et code archivé | Comparaison de contrats et capacités de référence | Aucune installation ou adoption automatique |

## Divergences et limites explicitement traitées
Les cinq boucles historiques et dix phases de leurs sources ne sont pas fusionnées avec W1–W10/T1–T2. Le nombre de rubriques d’une proposition n’altère pas les huit familles BASE. Les technologies, paramètres et services cités dans les sources ne constituent pas des faits de déploiement.

Le pointeur bootstrap à 1/1 et le curseur initial à 0/0 désignaient deux projections à des instants différents ; ADR-0002 qualifie la phrase historique A01. La capture n’invente pas les dates natives ou identifiants de conversation absents. Les réponses précédentes sont des archives et l’état actuel se lit dans STATUS et le checkpoint.

La politique client retire volontairement les états et migrations réservés au dépôt modèle. Les appels qui supposent encore leur présence constituent une incompatibilité de distribution, pas une autorisation de les recopier. Le diagnostic détaillé est dans CI_COMPATIBILITY.md.

## Critères de confiance
Décision propriétaire explicite, fait GitHub observé, fichier/contrat versionné, preuve de test et proposition ont des rôles différents. Les références aux repos externes gardent leur SHA. Une contradiction future reçoit sa disposition HOLD_FOR_REVIEW pour son périmètre ; les besoins non couverts restent dans le registre des demandes. La présente qualification suffit à préparer le contrat W1, sans prétendre achever la recherche historique exhaustive ni certifier le moteur.
