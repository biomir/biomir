# BioMIR Codex Handoff

_Last updated: 2026-09-03_

## Purpose
This file is the durable checkpoint for substantial Codex work. Read it at the start of a new thread and update it before ending a meaningful work unit. Keep it concise, current, and factual.

## Current objective
Establish a session-resilient Codex workflow so BioMIR development can continue across thread/context/session boundaries without relying on conversation history.

## Completed
- Added repository-level `AGENTS.md` with persistent operating instructions.
- Established scientific/clinical integrity requirements for health-related computation changes.
- Established HealthKit/data-integrity requirements.
- Established verification, Git, work-decomposition, and handoff requirements.
- Added this durable handoff file.

## Current engineering state
The durable Codex workflow is initialized. This checkpoint does **not** assert that the current BioMIR application has been fully built, tested, scientifically validated, or audited. A fresh development work unit should inspect the repository and establish the actual baseline before making those claims.

## Required baseline at next substantive work unit
1. Inspect repository structure and `git status`.
2. Review recent commits and identify the active application target/source tree.
3. Determine available build and test targets.
4. Run an initial build/test baseline where the environment permits it.
5. Inventory known high-priority scientific/computational and HealthKit issues from repository evidence rather than conversational memory.
6. Update this file with the verified baseline and the exact active objective.

## Verification for this checkpoint
Repository workflow files were created as configuration/documentation only. No application build or scientific validation is claimed by this checkpoint.

## Open risks / blockers
- Application build/test status has not yet been established in this checkpoint.
- Scientific validity of individual BioMIR algorithms must be evaluated against their specific implementation and evidence; repository workflow instructions do not constitute validation.
- Local-only work that has not been committed/pushed cannot be represented by this GitHub checkpoint and must be reconciled when Codex opens the local working tree.

## Next action
When a new Codex thread starts in the BioMIR working directory, ask it to: **read `AGENTS.md` and `CODEX_HANDOFF.md`, inspect the working tree and recent commits, establish the build/test baseline, update this handoff with verified current state, and only then resume the highest-priority BioMIR engineering task.**
