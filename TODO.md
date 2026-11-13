# TODO — Travail restant

## Automatic initialization

- [x] Provide deterministic manual initialization.
- [x] Provide automatic bootstrap workflow.
- [x] Provide bootstrap receipt and attestation.
- [x] Provide canonical-memory pointer and revision guards.
- [x] Provide multi-agent sessions, work claims and collision domains.
- [x] Provide dependency-safe deterministic dispatch.
- [x] Provide machine-readable checkpoints and handoff.
- [x] Provide new-information intake and contradiction hold-for-review.
- [x] Provide source-CI simulation of the automatic path.
- [x] Provide project-profile discovery with Chainsolutions full-stack candidate.
- [x] Represent absent/unprovisioned server, directory, domain and database state.
- [x] Prefer direct MCP server access with governed SSH fallback.
- [x] Route agent sessions by explicit connection intent.
- [x] Block mutable dispatch for context/information/unknown intents.
- [x] Add CI regression tests for capability intent and routing.

## Project instance first work

- [x] Resolve or explicitly defer the project profile in `.governance/project-profile.json`.
- [ ] Discover deployment target and access state in `.governance/infrastructure-intent.json`.
- [x] Complete `PROJECT_CONTEXT.md`.
- [x] Describe architecture in `docs/ARCHITECTURE.md`.
- [x] Define project acceptance criteria.
- [x] Identify initial risks and dependencies.
- [x] Capture project baseline and CI.
- [x] Replace generic baseline discovery with the first project-specific unique action.


## V2.2 entry workflow layer

- [x] Require an entry action on every governed agent connection.
- [x] Route new-repository creation separately from repo-local work.
- [x] Support organization and personal-account repository scopes.
- [x] Add plan-first additive adoption for existing repositories.
- [x] Add read-only current/target project mapping mode.
- [x] Add isolated lab branch/PR evolution mode.
- [x] Preserve normal governed-work continuation.
- [x] Add regression tests for routing, adoption preservation and repository scopes.


## V2.3 central control plane

- [x] Make Governed-Repository-Template the central preparation/control plane.
- [x] Persist interactive governed requests outside template content.
- [x] Add direct GitHub agent invocation through repository dispatch.
- [x] Ask one question or action request at a time.
- [x] Build action-specific chronological preparation packages.
- [x] Require explicit plan approval.
- [x] Validate preparatory evidence before advancing.
- [x] Produce explicit target handoff packages.
- [x] Keep generated/adopted repositories as clients, not duplicate control planes.
- [x] Add CI regression tests for control-plane lifecycle and source/client boundary.


## Demandes propres à Looping-
Le propriétaire détaillé est [docs/memory/REQUESTS.json](docs/memory/REQUESTS.json). Ce tableau et ses critères ne sont pas dupliqués ici. L’ordre et les sorties sont dans [ROADMAP.md](ROADMAP.md) ; la reprise globale est NEXT_ACTION.md. Les cases héritées du template décrivent son catalogue et ne certifient pas la réussite de chaque mécanisme dans cette instance.

- Conserver et faire évoluer les demandes documentées, en distinguant les capacités encore planifiées.
- Achever la qualification historique et les limites de capture : LOOP-REQ-005 / LOOP-REQ-015.
- Poursuivre la baseline et caractériser les blocages de portabilité : LOOP-FIND-001.
- Détailler les contrats de workflows puis le raccordement moteur : LOOP-REQ-003/004/007/008.

## Découverte qualifiée et restant
La baseline est possédée par docs/baseline/BASELINE.json. Le travail suivant est la spécification W1 ; les correctifs CI-B01/CI-B02 restent ouverts dans leur propriétaire, ainsi que les lacunes historiques. Les cases de découverte cochées ne signifient ni infrastructure observée ni CI complète réussie.
