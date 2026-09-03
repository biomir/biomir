# BioMIR — Codex Project Instructions

## Mission
Treat this repository as a persistent, high-integrity engineering project. Do not rely on conversation history as the sole source of project state. Preserve enough repository-level context that a new Codex thread can resume work safely and efficiently.

BioMIR is health/biomedical software. Changes affecting biomarkers, physiological interpretation, biological-age computations, HealthKit ingestion, units, reference ranges, scoring, or user-facing health claims require heightened scientific and engineering rigor.

## Start of every task
1. Read this `AGENTS.md`.
2. Read `CODEX_HANDOFF.md` if present.
3. Inspect `git status` and recent relevant commits before editing.
4. Identify the requested scope and the files/components it affects.
5. Preserve unrelated user changes; never discard work merely to obtain a clean tree.

## Persistent handoff discipline
For any substantial or multi-file task, maintain `CODEX_HANDOFF.md` as durable working state. Before ending a work unit, update it with:
- current objective and acceptance criteria;
- work completed;
- files/components changed;
- important scientific, clinical, product, or architectural decisions;
- assumptions that still require verification;
- build/test/static-analysis commands run and their exact outcome;
- unresolved defects, risks, and blockers;
- exact next actions in priority order.

Keep the handoff concise and factual. Replace stale status rather than accumulating a conversational diary. Never include secrets, credentials, tokens, private health records, or other sensitive data.

## Work decomposition
For large requests, work in bounded, independently verifiable units. Prefer this order when applicable:
1. data ingestion/provenance and unit normalization;
2. biomarker/domain computation;
3. scientific/clinical validation and reference tests;
4. persistence/state management;
5. UI/presentation and accessibility;
6. regression tests, performance, and cleanup.

Do not claim completion of a broad audit or refactor when only a subset has been inspected or changed. Record remaining scope in `CODEX_HANDOFF.md`.

## Scientific and clinical integrity
- Do not invent coefficients, thresholds, reference ranges, citations, validation results, or clinical interpretations.
- Distinguish published algorithms from BioMIR-specific adaptations or heuristics.
- Preserve explicit units and conversion logic at boundaries.
- Treat missing data, partial biomarker panels, clipping/winsorization, normalization, imputation, and fallback behavior as scientifically meaningful decisions.
- Avoid silent defaults that can change a health score or interpretation.
- When modifying KDM, PhenoAge, homeostatic dysregulation, ALI, BAI, CMA, ABA, or related algorithms, trace the formula end-to-end and add or update deterministic reference/golden tests where feasible.
- Do not describe an implementation as clinically validated unless the repository contains evidence supporting that claim.
- Flag uncertainty explicitly when evidence is insufficient.

## HealthKit/data integrity
- Preserve provenance, timestamps, units, aggregation windows, deduplication behavior, and source semantics.
- Avoid double counting overlapping samples or domains.
- Treat authorization failure, missing data, stale data, and partial synchronization as distinct states where relevant.
- Do not weaken privacy or permission handling for convenience.

## Engineering quality
- Prefer small, comprehensible changes over speculative rewrites.
- Follow existing Swift/SwiftUI architecture and naming unless a change has a documented reason.
- Keep computation out of presentation code when practical.
- Avoid duplicate sources of truth.
- Consider concurrency, cancellation, actor isolation, memory, and UI responsiveness when touching asynchronous or HealthKit code.
- Add regression tests for corrected defects when feasible.
- Do not suppress compiler warnings or errors merely to make checks pass.

## Verification
After changes, run the strongest applicable checks available in the repository/environment. At minimum:
- inspect the resulting diff;
- run relevant unit/reference tests when available;
- build/type-check the affected target when the environment supports it;
- report checks that could not be run and why.

Never state that a build or test passed unless it was actually executed successfully in the current work unit.

## Git discipline
- Make coherent, reviewable commits at validated milestones when the task/environment permits commits.
- Use descriptive commit messages.
- Do not rewrite existing history or force-push unless explicitly requested.
- Before finishing, inspect `git status` and clearly report any uncommitted or unrelated changes.

## Completion standard
A task is complete only when the requested scope is implemented or explicitly accounted for, relevant verification has been performed to the extent possible, material scientific/clinical risks are documented, and `CODEX_HANDOFF.md` contains enough state for a fresh Codex thread to continue without reconstructing the prior conversation.