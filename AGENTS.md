# VLN Research Repo Guidance

These instructions apply to the full repository.

## Language
- Use English by default for responses and saved documents.

## Scope
- Keep all project work inside this repository.
- Treat this repository as the canonical workspace for the VLN survey paper and the later CoRL method paper.

## Research Objectives
- Phase 1: complete a comprehensive VLN literature survey and prepare a survey paper targeting IEEE.
- Phase 2: identify high-value open problems in VLN, design a new method, and prepare a CoRL submission.

## Workflow Expectations
- Prefer installed research workflows and skills over ad hoc approaches.
- When available in the active session, prefer ARIS/Codex research workflows for:
  - literature search and synthesis
  - novelty checking
  - research review
  - paper planning and drafting
  - citation and claim audits
- Keep planning, literature synthesis, writing, and experiment artifacts clearly separated.

## Repository Hygiene
- Do not commit datasets, model weights, raw experiment outputs, or logs.
- Keep the directory structure clean and reproducible.
- Add durable notes and plans as Markdown files.

## HPC Assumptions
- Assume the login node has no GPU access.
- Do not run GPU-dependent experiments from the login node.
- Request GPU resources explicitly before any later experiment phase.
