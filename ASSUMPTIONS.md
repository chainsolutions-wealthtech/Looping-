# ASSUMPTIONS

No project-specific assumption is valid until recorded here with:
- identifier;
- statement;
- evidence;
- owner;
- date;
- validation status;
- invalidation condition.


## Hypothèses et choix explicitement non validés

| ID | Énoncé à qualifier | État | Preuve / propriétaire | Condition de réexamen |
|---|---|---|---|---|
| A-BASE-01 | Le candidat Node.js/Next.js/PostgreSQL convient à l’application future | NOT_VALIDATED — aucun choix actif | project-profile et ADR-0003 | Cahier des charges et contrats RP-04 |
| A-BASE-02 | Un raccordement MCP live existe pour ce dépôt | NOT_ESTABLISHED — binding unconfigured | mcp-binding ; aucune requête runtime | Découverte runtime autorisée et observée |
| A-BASE-03 | Les workflows hérités sont tous portables vers un client initialisé | DISPROVED_FOR_OBSERVED_PATHS | CI-B01/CI-B02 | Correctif et suites source/client exécutés |
| A-BASE-04 | Le corpus contient tous les anciens échanges bruts | NOT_ESTABLISHED — couverture partielle | CONVERSATION_LEDGER | Sources historiques supplémentaires retrouvées |
| A-BASE-05 | Des microservices et Kubernetes sont nécessaires au moteur | NOT_VALIDATED — références de conception | BASE et architecture | Besoins, contraintes et arbitrage explicites |

Les faits observés, reports explicites et hypothèses restent séparés. Les valeurs inconnues ne sont pas remplacées par des estimations non signalées.
