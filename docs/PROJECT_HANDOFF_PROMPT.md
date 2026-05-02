# VLN Project Handoff Prompt

Use this document as the starting prompt for a new conversation. It is intended to transfer the full current project state, the non-negotiable constraints, the completed results, the remaining gaps, and the exact next steps.

## Identity and Scope

You are continuing a VLN research project inside:

- `/home/hxfeng/fhx-corl-2026`

This repository is the only allowed workspace for this project. Do not inspect, modify, or rely on any other project directory. All work must stay inside this repository.

## Default Language

- Use English by default for all responses and saved documents.
- Switch language only if explicitly requested.

## Repository and Git Workflow Requirements

- This repository is the canonical project workspace.
- Prefer one dedicated GitHub repository per project.
- After meaningful changes, commit and push promptly.
- Commit messages must be in English.
- Follow the Lore-style commit discipline already used in this repo.
- Do not commit datasets, model weights, logs, intermediate experiment outputs, or other large non-reproducible artifacts.
- Keep the repository clean and minimal.

Remote:

- `origin https://github.com/fhx020826/fhx-corl-2026.git`

Current branch:

- `main`

## Environment Assumptions

- Assume this machine is an HPC login node unless evidence shows otherwise.
- Do not assume GPU access on the login node.
- Request GPU resources explicitly before any future experiment phase.
- Prefer the configured proxy for external network access when available.

## High-Level Research Program

This is a two-stage VLN research program:

1. produce a high-quality VLN survey paper, originally intended toward IEEE-style publication
2. use the survey to identify important open VLN problems and later produce a new method paper targeting CoRL

At the end of the current conversation, only the literature/survey phase has been executed. No method implementation or experiment phase has started.

## Original User Requirements That Must Still Be Respected

The user’s core requirements were:

1. Build a comprehensive VLN-related paper list.
2. Start from VLN surveys, including broader embodied-navigation surveys where relevant.
3. Use the papers cited by those surveys as the first expansion frontier.
4. Expand further using:
   - arXiv
   - keyword search
   - Google Scholar-style search
   - curated GitHub repositories such as `awesome-vln`
5. Avoid imposing a taxonomy before collection.
6. Collect broadly first; taxonomy comes later.
7. The final list should be as comprehensive as possible.
8. The user explicitly expected the paper inventory to eventually reach at least `200+` papers.
9. The final delivered table must be directly usable in Feishu and include:
   - serial number
   - full title
   - publication date
   - venue
   - newest-to-oldest ordering
10. The final strict deliverable should contain VLN-related papers only, excluding obvious non-VLN papers from other directions such as broader VLA-style or unrelated embodied papers.

## Important Methodological Corrections Learned During the Project

Several mistakes happened during the project and must not be repeated:

1. The collection process initially became too dependent on:
   - `awesome-vln`
   - exact-title arXiv sweeps
   - manually chosen search phrases

2. That process produced a broad corpus, but it missed important direct VLN papers such as:
   - `DualVLN`
   - other recent direct VLN frontier papers

3. The earlier broad corpus also mixed direct VLN papers with broader boundary papers such as:
   - embodied AI surveys
   - general navigation platforms
   - embodied QA and other neighboring but non-VLN tasks

4. Therefore, a strict final pass was necessary to:
   - add missing direct VLN papers
   - exclude obvious non-VLN papers from the final delivered list

This means:

- the broad working corpus was useful as a search surface
- but the strict final VLN-only list is the actual primary deliverable

## What Was Completed, In Order

### 1. Project setup and repository preparation

The repo was created and linked to GitHub. Project guidance and planning documents were written.

### 2. Survey-of-surveys stage

A survey-scoping note was created to identify the major VLN and embodied-navigation survey seeds and compare how they organize the field.

Preserved supporting file:

- `docs/VLN_SURVEY_OF_SURVEYS.md`

This file remains useful because it documents the trusted survey seeds and the logic behind them.

### 3. Broad corpus-building stage

The project then built a broad VLN-related corpus through several rounds:

- survey-seeded expansion
- `awesome-vln` parsing
- arXiv search
- targeted frontier backfill
- direct-title sweep for many 2024–2026 papers

This broad working corpus exceeded 200 papers, but it was not strict enough for the final deliverable because it still contained some non-VLN boundary items.

### 4. Feishu-ready working artifacts

Intermediate Feishu-oriented files were created for the broader corpus, but they were later superseded and removed during cleanup.

### 5. Final strict completeness audit

A strict final audit was performed to fix two issues:

- direct high-signal VLN papers were still missing
- obvious non-VLN boundary papers were still included

The final strict audit added these important missing papers:

- `Ground Slow, Move Fast: A Dual-System Foundation Model for Generalizable Vision-and-Language Navigation`
- `DV-VLN: Dual Verification for Reliable LLM-Based Vision-and-Language Navigation`
- `SE-VLN: A Self-Evolving Vision-Language Navigation Framework Based on Multimodal Large Language Models`
- `DELAN: Dual-Level Alignment for Vision-and-Language Navigation by Cross-Modal Contrastive Learning`
- `Vision-Language Navigation Policy Learning and Adaptation`
- `Counterfactual Vision-and-Language Navigation: Unravelling the Unseen`
- `Self-Motivated Communication Agent for Real-World Vision-Dialog Navigation`

The strict audit also explicitly excluded obvious non-VLN boundary items from the final deliverable.

### 6. Final strict deliverables

The final strict VLN-only paper list was generated in three formats:

- Markdown
- TSV
- CSV

An audit note was also written documenting the final additions and exclusions.

### 7. Repository cleanup

The repository was then cleaned thoroughly:

- outdated planning artifacts removed
- superseded intermediate working lists removed
- placeholder directory READMEs removed
- empty placeholder directories removed
- top-level documentation updated to point directly at the final deliverables

## Current Final Deliverables

These are the key files that must be preserved and treated as canonical:

1. Strict final Markdown paper list:
   - `references/vln-paper-list-final-strict.md`

2. Strict final TSV paper list for direct Feishu paste:
   - `references/vln-paper-list-final-strict.tsv`

3. Strict final CSV paper list:
   - `references/vln-paper-list-final-strict.csv`

4. Final audit note:
   - `docs/VLN_FINAL_COMPLETENESS_AUDIT.md`

5. Survey-of-surveys supporting note:
   - `docs/VLN_SURVEY_OF_SURVEYS.md`

## Current Repository Surface

After cleanup, the meaningful file surface is intentionally small:

- `README.md`
- `AGENTS.md`
- `docs/VLN_FINAL_COMPLETENESS_AUDIT.md`
- `docs/VLN_SURVEY_OF_SURVEYS.md`
- `references/README.md`
- `references/vln-paper-list-final-strict.md`
- `references/vln-paper-list-final-strict.tsv`
- `references/vln-paper-list-final-strict.csv`

## Current Final Result

The strict final VLN-only list currently contains:

- `200` papers

Important characteristics:

- intended to be VLN-related only
- ordered newest to oldest
- includes 2025 and 2026 papers
- includes serial number, title, date, and venue in the final deliverable formats
- preserves `*` for provisional dates where date normalization remains incomplete

## Important Remaining Limitations

Even though the final strict deliverable is much better than the earlier mixed corpus, there are still limitations that a future conversation should understand clearly:

1. The list is strong, but no one should claim literal internet-perfect completeness.
2. Some venue labels are still broad or fallback-style, especially for newer papers:
   - many newer entries are labeled `arXiv preprint`
3. Some provisional dates still remain marked with `*`.
4. A future pass could still discover additional 2026 VLN papers, especially if new ones appeared after the current audit.
5. The strict list should be treated as the main deliverable, but the audit note should be read alongside it.

## Why DualVLN Was Missed Earlier

This must be remembered because it explains the weakness of the earlier pipeline:

- the earlier broad search process relied too much on curated repositories and exact-title arXiv sweeps
- it did not perform a sufficiently strong frontier-system audit over project pages, OpenReview, and system-name-based search
- `DualVLN` is exactly the kind of paper that can be missed if search depends too much on older survey references and curated lists

This is why the strict final audit explicitly corrected the omission.

## Files Removed During Cleanup

The following categories were intentionally removed because they were outdated, superseded, or intermediate:

- old working corpora
- intermediate Feishu exports
- preparation-only planning files
- placeholder `README.md` files for empty directories
- empty placeholder directories

This was deliberate and should not be undone casually.

## Current Project Status

Status:

- literature review deliverable completed in a strong strict form
- survey-of-surveys note preserved
- repo cleaned
- no taxonomy document finalized
- no survey manuscript draft written yet in this cleaned repo state
- no method-planning or CoRL experiment phase started

## Recommended Next Steps In A New Conversation

If continuing the project in a new conversation, the next step should depend on the user’s goal:

### If the goal is bibliographic polishing

Do this next:

1. audit all `Venue` fields in `references/vln-paper-list-final-strict.*`
2. normalize entries currently labeled only as `arXiv preprint`
3. verify all `*` provisional dates
4. improve bibliographic fidelity without changing the strict VLN-only scope unless new clear VLN papers are found

### If the goal is survey writing

Do this next:

1. read:
   - `docs/VLN_SURVEY_OF_SURVEYS.md`
   - `docs/VLN_FINAL_COMPLETENESS_AUDIT.md`
   - `references/vln-paper-list-final-strict.md`
2. induce a post-collection taxonomy from the final strict corpus
3. produce:
   - survey outline
   - section plan
   - benchmark/task/method structure

### If the goal is research-gap extraction

Do this next:

1. use the final strict corpus as the only primary evidence base
2. cluster the literature by:
   - task setting
   - environment
   - benchmark
   - planning/memory/reasoning
   - dialog/interactivity
   - aerial/outdoor/continuous/generalization
3. identify under-solved high-value directions for a later CoRL paper

## Non-Negotiable Rules For Future Continuation

1. Work only inside `/home/hxfeng/fhx-corl-2026`.
2. Use English by default.
3. Keep the repository clean.
4. Do not reintroduce deleted intermediate artifacts unless there is a very strong reason.
5. Treat the strict final paper list as canonical.
6. Do not quietly widen the scope back to broad embodied AI, VLA, or generic platform papers in the final deliverable.
7. Keep commit messages in English and push meaningful changes promptly.

## Exact Files To Start From

If starting from scratch in a new conversation, begin by reading these files in order:

1. `README.md`
2. `docs/VLN_FINAL_COMPLETENESS_AUDIT.md`
3. `docs/VLN_SURVEY_OF_SURVEYS.md`
4. `references/vln-paper-list-final-strict.md`
5. `references/vln-paper-list-final-strict.tsv`

## Short Restart Prompt

If you need a shorter version to begin a new conversation, use this:

> Continue the VLN project in `/home/hxfeng/fhx-corl-2026`. Use English by default. Only work inside this repo. The cleaned final deliverables are `references/vln-paper-list-final-strict.md`, `references/vln-paper-list-final-strict.tsv`, `references/vln-paper-list-final-strict.csv`, plus `docs/VLN_FINAL_COMPLETENESS_AUDIT.md` and `docs/VLN_SURVEY_OF_SURVEYS.md`. The strict final list has 200 VLN-related papers and excludes obvious non-VLN boundary papers. Important earlier mistake: the broader corpus missed direct papers like DualVLN and mixed in non-VLN boundary items, so do not revert to that broader, noisier scope. Preserve repo cleanliness, commit in English, and push meaningful changes promptly. Start by understanding the current deliverables and then continue with either venue/date normalization, survey writing, or research-gap extraction.

