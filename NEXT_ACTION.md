# NEXT_ACTION — Point de reprise unique

```text
NEXT_ACTION = DISCOVER_PROJECT_BASELINE
STATE = IN_PROGRESS
```

## Action
Poursuivre la qualification de la baseline de Looping- à partir de la mémoire canonique et de la roadmap RP-02 : comparer les sources, l’architecture initiale, les mécanismes réellement présents et les blocages CI. Examiner la frontière source/client avant de proposer un correctif ; ne pas recopier aveuglément les états source-only manquants.

Le contexte, la méthode, le registre des demandes et l’architecture documentaire sont désormais renseignés. Les observations exactes et la publication du lot se reprennent dans docs/memory/CHECKPOINT.json. Réobserver HEAD, permissions et modifications concurrentes avant toute écriture. Le premier contrat à détailler ensuite est W1, constitution et coordination documentaire.

## Done when
- sources et propositions qualifiées avec provenance et contradictions explicites ;
- profil technique sélectionné ou explicitement différé ;
- serveur, domaine, répertoire et base observés ou laissés non résolus avec leur justification ;
- contexte, architecture, risques, dépendances et critères métier suffisamment définis ;
- baseline HEAD/CI et défauts hérités enregistrés, sans fausse réussite ;
- conditions de passage vers le premier contrat W1 établies ;
- première action fonctionnelle suivante définie sans créer une seconde file.

La présente entrée ne ferme pas WORK-DISCOVER-001 et n’accorde aucune autorité code ou infrastructure.
