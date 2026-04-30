# Workflow Map

This file maps the planned VLN program to the installed research-oriented skills and agent roles that should be preferred during execution.

## Rule of use

- Stay in preparation mode until the user explicitly starts the research execution phase.
- Prefer the lightest workflow that still preserves rigor.
- Use repo-local artifacts as the source of truth for scope, plans, and writing.

## Phase-to-workflow routing

### 1. VLN survey scoping

Primary route:
- `literature-reviewer`

Supporting route:
- `researcher`
- ARIS-style `research-lit`

Use this phase to decide:
- what counts as VLN for this survey
- which neighboring areas are in scope or out of scope
- which venues and years must be covered

Expected artifacts:
- scope statement
- taxonomy
- inclusion and exclusion policy

### 2. Full literature coverage

Primary route:
- `literature-reviewer`

Supporting route:
- ARIS-style `research-lit`
- ARIS-style `research-review`

Use this phase to build:
- a paper inventory
- thematic groupings
- benchmark and metric comparisons
- contradiction and gap notes

Expected artifacts:
- curated inventory
- comparison matrix
- synthesis notes

### 3. IEEE survey paper

Primary route:
- ARIS-style `paper-plan`
- ARIS-style `paper-write` or `paper-writing`

Supporting route:
- ARIS-style `paper-figure`
- ARIS-style `paper-claim-audit`
- ARIS-style `citation-audit`
- `writer`

Use this phase to enforce:
- claim-evidence discipline
- section-level planning before drafting
- citation verification before submission

Expected artifacts:
- outline
- manuscript draft
- figure list
- claim audit
- citation audit

### 4. Problem extraction and idea generation

Primary route:
- ARIS-style `idea-creator`
- ARIS-style `novelty-check`

Supporting route:
- `literature-reviewer`
- ARIS-style `research-review`

Use this phase to rank:
- novelty
- feasibility
- CoRL fit
- evaluation clarity

Expected artifacts:
- ranked problem list
- shortlisted method directions

### 5. Method and experiment planning

Primary route:
- ARIS-style `experiment-plan`
- ARIS-style `ablation-planner`

Supporting route:
- `architect`
- `test-engineer`

Use this phase to define:
- baselines
- datasets
- metrics
- ablations
- compute budget

Expected artifacts:
- experiment plan
- ablation matrix
- resource budget

### 6. Execution and iteration

Primary route:
- `executor`
- ARIS-style `run-experiment`
- ARIS-style `monitor-experiment`

Supporting route:
- ARIS-style `analyze-results`
- ARIS-style `result-to-claim`
- ARIS-style `auto-review-loop`

Use this phase to enforce:
- reproducible implementation
- pilot-before-scale
- result-to-claim traceability

Expected artifacts:
- reproducible code
- validated results
- improvement loop history

### 7. CoRL paper

Primary route:
- ARIS-style `paper-plan`
- ARIS-style `paper-write` or `paper-writing`

Supporting route:
- ARIS-style `paper-figure`
- ARIS-style `paper-claim-audit`
- ARIS-style `citation-audit`

Expected artifacts:
- paper draft
- appendix plan
- final audit reports

## When to use standard non-ARIS roles

- `explore`: repo-local lookup only
- `researcher`: official external docs or venue rules
- `writer`: clean prose, revision, and structure polishing
- `architect`: system design for the method codebase
- `executor`: implementation
- `verifier`: completion checks before claiming a phase is done

## Hard stops

- Do not start literature collection until the scope statement is approved.
- Do not start method design until the survey phase is materially complete.
- Do not start GPU experiments from the login node.
- Do not treat any draft as ready without citation and claim audits.
