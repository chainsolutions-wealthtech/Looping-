# Vérification de l’intégration documentaire

Date d’observation : 2026-11-13T06:49:33+00:00.

## Ancrage vérifié
- Dépôt : chainsolutions-wealthtech/Looping- ; branche main.
- Baseline : 86f0317905eb1eaf790e4f2f58a7e3e41735c2bf ; arbre 3be10c4806e95b171051687780541fef9818a5c7.
- Commit d’import : [217f2380d19dc9b67eb60aef848c42ae7171062f](https://github.com/chainsolutions-wealthtech/Looping-/commit/217f2380d19dc9b67eb60aef848c42ae7171062f).
- Arbre d’import : fd1df663a49eb5c4b21b75a860c2ba0f5c6f3500.
- Parent unique : baseline ci-dessus ; mise à jour de main effectuée sans force, avec expected_sha exact. La relecture de main a retrouvé le commit d’import.

Ce document rapporte les contrôles du commit d’import. Le commit qui ajoute ce compte rendu ne change ni le curseur ni la disposition de l’intake.

## Contrôles du dossier

| Contrôle | Résultat observé |
|---|---|
| Périmètre de l’import | 28 ajouts, deux modifications : SUIVI.md et .governance/intake/cursor.json |
| Conservation de l’existant | Aucune suppression ; empreintes et modes des autres fichiers inchangés |
| Arbre Git distant | 30 blobs attendus retrouvés avec leurs empreintes exactes |
| Relecture des documents principaux | Sept contenus relus au commit d’import et identiques à la préparation |
| Registre BASE | 55 identifiants uniques, 54 liens parentaux, 28 relations ; références valides |
| Provenance | 17 sources enregistrées ; 14 snapshots GitHub comparés à leurs blobs d’origine |
| Textes originaux | Neuf messages source et document consolidé conservés ; décodage JSON vérifié sans perte |
| Données d’intake | INTAKE-0001 RECEIVED / UNASSESSED ; canonical_effect=false et work_effect=false |
| Révisions | canonical_revision=0 ; work_revision=0 ; une entrée en attente de réconciliation |
| Intégrité textuelle locale | Contrôle des 30 fichiers préparés réussi après représentation JSON des textes originaux |

## Résultats GitHub Actions du commit d’import

| Exécution | Résultat | Preuve |
|---|---|---|
| Governance CI | FAILURE | [43381121164](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43381121164) |
| Governed Agent Continuity Relay | FAILURE | [43381121244](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43381121244) |
| GSCC Observable Arrival Gateway | FAILURE | [43381121167](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43381121167) |
| GSCC Function Exposure Gate | SUCCESS | [43381121258](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43381121258) |
| Governance Auto Bootstrap | SUCCESS | [43381121106](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43381121106) |
| GSCC Function Route Selftest | SKIPPED | [43381121058](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43381121058) |

Dans Governance CI, la validation de structure, la compilation, le protocole GSCC/SessionEndpoint et la capture first-touch exhaustive ont réussi. L’exécution s’arrête ensuite au test de base first-touch ; les contrôles suivants sont SKIPPED. La CI complète ne peut donc pas être déclarée réussie.

## Blocages attestés dans les journaux
- Job 131738854565, Governance CI : FileNotFoundError sur .governance/control-plane-db/007_first_touch_field_block_gate.sql.
- Job 131738855156, Observable Arrival : FileNotFoundError sur le même fichier SQL.
- Job 131738855238, Continuity Relay : FileNotFoundError sur .governance/control-plane-state/namespace-work-registry.json.

Ces deux chemins sont absents des arbres complets de la baseline et de l’import. Ils n’ont pas été supprimés par cet intake. Les journaux ont été lus ; la conclusion porte sur les points d’arrêt observés, sans prétendre avoir reproduit toute la suite sur la baseline ni connaître tous les blocages suivants.

## Suite rattachée au dossier
Évaluer la cohérence de l’intake, qualifier les exigences et traiter les manques de baseline dans leur périmètre avant toute promesse d’exécution automatique. La prochaine action globale reste DISCOVER_PROJECT_BASELINE ; celle du dossier reste EVALUATE_INTAKE_COHERENCE. Les sources importées et les propositions ne sont pas promues automatiquement en autorités, décisions ou tâches.
