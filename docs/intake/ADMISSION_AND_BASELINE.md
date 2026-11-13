# Entrée observée et baseline

- Cible explicite : chainsolutions-wealthtech/Looping-.
- Compte connecté observé : Patricked-code, ID GitHub 270385782.
- Permissions retournées sur la cible : admin/maintain/push/pull/triage à true.
- Branche canonique documentée : main.
- HEAD observé pour la préparation : 86f0317905eb1eaf790e4f2f58a7e3e41735c2bf.
- Arbre Git observé : 3be10c4806e95b171051687780541fef9818a5c7 ; réponse récursive non tronquée, 362 entrées.
- État de projet : GOVERNANCE_INITIALIZED_BASELINE_REQUIRED.
- NEXT_ACTION existante : DISCOVER_PROJECT_BASELINE.
- Cursor intake observé : séquence 0, révisions canonique et work à 0.
- Aucune branche de travail ou PR ouverte observée à l’inventaire initial.

## Entrée GSCC réellement tentée
Issue créée conformément à la porte A : [#1](https://github.com/chainsolutions-wealthtech/Looping-/issues/1).
Les références privées de conversation/session non exposées ont été marquées UNAVAILABLE ; aucun identifiant fournisseur n’a été inventé.

- [Provider First Touch Ingress — run 43376454383](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43376454383) : failure.
- Job ingest 131723965825 : échec à « Materialize existing B00-B30 first-touch database » ; release ignorée.
- [Observable Arrival — run 43376454394](https://github.com/chainsolutions-wealthtech/Looping-/actions/runs/43376454394) : failure.
- Job arrival 131723966084 : échec à « Materialize first-touch field block gate database ».
- Aucun commentaire de release dans l’issue lors de l’observation.
- Les logs détaillés ne sont pas exposés par la route de lecture disponible ; aucune cause technique exacte n’est affirmée.

## Écart statique distinct
Le workflow First Touch référence quatre migrations absentes de l’arbre cible observé : 008_gscc_observable_entry_pipeline.sql, 009_gscc_post_q1_gate_route.sql, 010_gscc_arrival_session_identity.sql et 011_gscc_session_runtime.sql sous .governance/control-plane-db/. Cet écart est constaté séparément ; il n’est pas présenté comme la cause démontrée du premier échec.

## Condition d’écriture
AGENTS.md et 00_GSCC_ENTRY.md exigent une release GSCC, ou la porte B choisie explicitement selon 00_DIRECT_OWNER_ENTRY.md.
Lors de la préparation initiale, la porte B n’était pas sélectionnée. Elle est maintenant confirmée par U09 et validée sur les faits GitHub ci-dessous. Cette porte indépendante ne vaut pas admission GSCC.
La porte B permet un intake direct avec authentification réelle, permissions natives, HEAD exact et trace GitHub, si le propriétaire la sélectionne explicitement. Aucune permission supplémentaire, aucun claim ou reçu GSCC n’est fabriqué.

## Limite
Ce dossier préparatoire ne modifie pas les politiques d’entrée. Les fichiers du dépôt n’ont pas été modifiés par la préparation ; l’issue d’arrivée constitue la trace distante réellement créée.

## Validation de la porte B après confirmation U09

- Confirmation conservée dans CONVERSATION_INPUTS.md, U09.
- Compte réellement connecté : Patricked-code, GitHub ID 270385782.
- Permissions du dépôt cible revérifiées : push/pull/admin/maintain/triage à true.
- HEAD main revérifié : 86f0317905eb1eaf790e4f2f58a7e3e41735c2bf ; protected=false observé.
- Décision de la route directe : DIRECT_OWNER_VERIFIED, portée INFORMATION_INTAKE.
- Preuves et réconciliation du literal de dépôt hérité : DIRECT_OWNER_ENTRY_EVIDENCE.json.
- Aucun reçu GSCC ni identité/session GACR n’est revendiqué. L’échec de la porte A reste historique et n’est pas transformé en succès.
