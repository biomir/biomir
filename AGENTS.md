# BioMIR — Codex Xcode-Only Instructions

## Hard scope boundary
Codex is assigned exclusively to BioMIR Xcode development.

Only perform work that directly concerns the BioMIR Apple-platform application and its Xcode project: Swift, SwiftUI, HealthKit integration, Apple frameworks, app resources, entitlements/capabilities, Xcode project/workspace configuration, build settings, package dependencies used by the Xcode app, XCTest/Swift Testing, compiler diagnostics, runtime defects, performance, accessibility, and application UI behavior.

Do NOT work on business strategy, commercialization, marketing, website/content, LinkedIn/social content, patents/IP strategy, CVs, job search, scientific posters, general research, GitHub portfolio projects unrelated to the Xcode app, administrative work, or other non-Xcode tasks.

If a request is outside this boundary, do not execute it. State that it is outside the Codex Xcode scope and leave repository state unchanged.

A scientific or clinical question is in scope only when necessary to inspect, validate, test, or correct behavior implemented in the BioMIR Xcode application. Do not independently initiate general scientific research.

## Mission
Maintain the BioMIR Xcode application as a high-integrity biomedical software project. Do not rely on conversation history as the sole source of project state.

Changes affecting biomarkers, physiological interpretation, biological-age computations, HealthKit ingestion, units, reference ranges, scoring, or user-facing health claims require heightened scientific and engineering rigor.

## Xcode integration
When Xcode tools are available, use them as the primary source of truth for Xcode-specific diagnostics and verification. Inspect the actual open project/workspace, compiler diagnostics, target configuration, and build/test results rather than inferring them from filenames alone.

Do not claim that an Xcode build, test, warning, or runtime issue is resolved unless the applicable verification was actually performed.

## Start of every task
1. Read this `AGENTS.md`.
2. Read `CODEX_HANDOFF.md` if present.
3. Inspect `git status` and recent relevant commits before editing.
4. Confirm that the requested work is within the Xcode-only boundary.
5. Identify the affected Xcode target, Swift/SwiftUI files, resources, tests, capabilities, or configuration.
6. Preserve unrelated user changes; never discard work merely to obtain a clean tree.
7. Prefer reproducing or observing the reported Xcode issue before changing code when practical.

## Persistent handoff discipline
For substantial or multi-file Xcode work, maintain `CODEX_HANDOFF.md` as durable working state. Before ending a work unit, update it with:
- current Xcode issue/objective and acceptance criteria;
- reproduction evidence or diagnostic messages;
- work completed;
- files/targets/components changed;
- important scientific, clinical, UI, or architectural decisions;
- assumptions requiring verification;
- Xcode build/test/static-analysis commands or tools run and exact outcomes;
- unresolved compiler/runtime/UI defects, risks, and blockers;
- exact next Xcode actions in priority order.

Keep the handoff concise and factual. Replace stale status rather than accumulating a conversational diary. Never include secrets, credentials, tokens, or private health records.

## Work decomposition
For large Xcode requests, use bounded, independently verifiable units. Prefer this order when applicable:
1. reproduce/characterize the Xcode issue;
2. data ingestion/provenance and unit normalization;
3. biomarker/domain computation;
4. scientific/clinical implementation validation and reference tests;
5. persistence/state/concurrency;
6. SwiftUI/UI behavior and accessibility;
7. regression tests, build verification, performance, and cleanup.

Do not claim completion of a broad audit or refactor when only a subset has been inspected or changed. Record remaining Xcode scope in `CODEX_HANDOFF.md`.

## Scientific and clinical integrity
- Do not invent coefficients, thresholds, reference ranges, citations, validation results, or clinical interpretations.
- Distinguish published algorithms from BioMIR-specific adaptations or heuristics.
- Preserve explicit units and conversion logic at boundaries.
- Treat missing data, partial biomarker panels, clipping/winsorization, normalization, imputation, and fallback behavior as scientifically meaningful decisions.
- Avoid silent defaults that can change a health score or interpretation.
- When modifying KDM, PhenoAge, homeostatic dysregulation, ALI, BAI, CMA, ABA, or related implementations, trace the formula end-to-end and add/update deterministic reference tests where feasible.
- Do not describe an implementation as clinically validated unless evidence supports that claim.
- Flag uncertainty explicitly when evidence is insufficient.

## HealthKit/data integrity
- Preserve provenance, timestamps, units, aggregation windows, deduplication behavior, and source semantics.
- Avoid double counting overlapping samples or domains.
- Treat authorization failure, missing data, stale data, and partial synchronization as distinct states where relevant.
- Do not weaken privacy or permission handling for convenience.

## Engineering quality
- Prefer the smallest correct fix over speculative rewrites.
- Follow existing Swift/SwiftUI architecture and naming unless a change has a documented reason.
- Keep computation out of presentation code when practical.
- Avoid duplicate sources of truth.
- Consider Swift concurrency, cancellation, actor isolation, memory, lifecycle, and UI responsiveness when relevant.
- Add regression tests for corrected defects when feasible.
- Do not suppress compiler warnings/errors merely to make checks appear clean.
- Do not modify unrelated files opportunistically.

## Verification
After changes, run the strongest applicable Xcode checks available. At minimum:
- inspect the resulting diff;
- build/type-check the affected target when possible;
- run relevant unit/reference/UI tests when available;
- inspect remaining Xcode diagnostics relevant to the change;
- report checks that could not be run and why.

Never state that a build or test passed unless it was actually executed successfully in the current work unit.

## Git discipline
- Make coherent, reviewable commits at validated Xcode milestones when permitted.
- Use descriptive commit messages.
- Do not rewrite history or force-push unless explicitly requested.
- Before finishing, inspect `git status` and report uncommitted or unrelated changes.

## Completion standard
An Xcode task is complete only when the requested issue is implemented or explicitly accounted for, applicable verification has been performed to the extent possible, material scientific/clinical/software risks are documented, and `CODEX_HANDOFF.md` contains enough state for a fresh Codex thread to continue the Xcode work without reconstructing prior conversation.