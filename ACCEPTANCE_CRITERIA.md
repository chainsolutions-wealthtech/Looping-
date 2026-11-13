# ACCEPTANCE_CRITERIA

## Repository governance

- [x] Project initialized.
- [x] Source-of-truth hierarchy explicit.
- [x] Architecture documented.
- [x] Baseline captured.
- [x] CI / validation strategy defined.
- [ ] No unresolved placeholders.
- [x] First project-specific acceptance criteria added.
- [x] Project profile discovered or explicitly deferred without inventing implementation.
- [x] Server/domain/directory/database state observed or left explicitly unresolved.
- [ ] Server access route resolved as direct MCP, SSH fallback, or unavailable.
- [ ] Agent connection intent resolved before mutable dispatch.

## Project acceptance

| Critère | État à la découverte | Propriétaire de preuve |
|---|---|---|
| Sources et base identifiées avec provenance | QUALIFIED_WITH_LIMITS | SOURCE_QUALIFICATION et ledger |
| Mémoire et registre de demandes présents | DOCUMENTED | Mémoire, REQUESTS et checkpoint |
| Profil et infrastructure explicitement différés | DOCUMENTED_DEFERRED | ADR-0003 et projections |
| Contexte, architecture, risques et dépendances initiaux | DOCUMENTED | Propriétaires à la racine et ARCHITECTURE |
| Baseline HEAD/CI capturée et échecs qualifiés | CAPTURED_WITH_KNOWN_DEFECTS | BASELINE et CI_COMPATIBILITY |
| Contrat W1 complet et traçable | PENDING | WORK-SPEC-W1-001 et NEXT_ACTION |
| Moteur BASE raccordé et boucle démontrée | NOT_IMPLEMENTED_OR_VERIFIED | Phases RP-05/RP-06 |
| CI complète et itération initiale GREEN | OPEN_BLOCKED | Runs exacts et CURRENT_ITERATION |
| Runtime, livraison et exploitation vérifiés | NOT_ATTESTED | Gates propres aux lots futurs |

Les sections suivantes sont héritées du template et portent ses références historiques. Leurs cases cochées ne constituent pas une certification de cette instance ; les critères de Looping- ci-dessus et les runs du checkpoint portent l’état actuel.


## Central control plane acceptance

- [x] Source template role is `CENTRAL_GOVERNANCE_CONTROL_PLANE`.
- [x] Generated/adopted target role is `GOVERNED_TARGET_CLIENT`.
- [x] Source-only workflow and issue form do not survive target initialization/adoption.
- [x] `governed_request_start` issue-creation contract is executed in CI and the source workflow exposes the repository-dispatch trigger.
- [x] The request engine emits exactly one next question/action/handoff.
- [x] Target mutation cannot begin before authority and plan approval.
- [x] Invalid or missing evidence cannot advance the state machine.
- [x] All five entry workflows can reach a valid `HANDOFF_READY`.
- [x] The final handoff includes target repository, branch/HEAD when known, allowed next operation, evidence and constraints.
- [x] Existing V2.0/V2.1/V2.2 regression tests remain GREEN.

Evidence:
- Governance CI run `36085243348`: all regression and V2.3 control-plane tests PASS.
- Live Governed Control Plane issue `#1`: issue-opened initialization PASS and issue-comment transition from revision 1 to revision 2 PASS.
- Live control-plane runs `36085152997`, `36085185770`, and `36085220470`: SUCCESS.


## Repository creation executor acceptance

- [x] CREATE flow asks owner first.
- [x] CREATE flow asks repository name second.
- [x] CREATE flow asks `private` or `public` third.
- [x] CREATE flow does not ask generic connection intent before creation.
- [x] Patricked display choice resolves to canonical GitHub owner `Patricked-code`.
- [x] PREP-001 uses GitHub REST `generate from template`.
- [x] Executor refuses missing creator credentials.
- [x] Executor verifies authenticated principal and private-template access.
- [x] Executor refuses an already-existing target.
- [x] Executor records observed initial HEAD after successful creation.
- [x] CI simulates successful creation paths for all configured owners.
