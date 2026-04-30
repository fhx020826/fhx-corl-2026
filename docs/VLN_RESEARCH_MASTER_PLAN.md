# VLN Research Master Plan

## Objective

Build a disciplined two-stage VLN research program:

1. produce a high-quality VLN survey paper suitable for IEEE submission
2. derive a defensible new VLN research direction and execute it toward a CoRL submission

This document is a preparation artifact only. It does not start the actual research workflow.

## Phase Structure

### Phase 0: Project Preparation

Goal: make the repository and workflow ready before any literature review or research execution.

Tasks:
- establish repository hygiene and ignore rules
- define the research workflow, artifact boundaries, and publication targets
- keep the repo ready for ARIS-style literature, planning, and writing workflows

Exit criteria:
- repo exists and is linked to GitHub
- project guidance exists
- master research plan exists

### Phase 1: VLN Survey Scoping

Goal: define the exact scope of the survey before collecting papers.

Planned workflow:
- use `literature-reviewer` for systematic scoping and search framing
- use ARIS-style `research-lit` workflow for broad collection and initial thematic grouping
- use `paper-miner` only after a strong core set of papers exists

Concrete outputs:
- scope statement
- inclusion and exclusion criteria
- venue list
- year range policy
- taxonomy draft for VLN subtopics

Recommended skill/agent routing:
- `literature-reviewer`
- `researcher` for official venue and benchmark details
- ARIS `research-lit`

Exit criteria:
- scope and taxonomy are stable enough to support full collection

### Phase 2: Comprehensive VLN Literature Review

Goal: collect and organize the full VLN paper landscape.

Planned workflow:
- search recent and foundational VLN papers
- organize papers by task setting, environment, modality, supervision, planner architecture, memory design, evaluation protocol, and embodiment assumptions
- identify benchmark drift, metric inconsistencies, and under-covered settings

Concrete outputs:
- curated paper inventory
- comparison matrix
- thematic synthesis notes
- benchmark and metric map
- unresolved contradiction list

Recommended skill/agent routing:
- `literature-reviewer`
- `research-knowledge-curator-obsidian` if project-local knowledge curation is later enabled
- ARIS `research-lit`
- ARIS `research-review`

Exit criteria:
- the literature inventory is broad enough to support a survey without obvious coverage gaps

### Phase 3: IEEE Survey Paper Production

Goal: convert the literature review into a rigorous survey manuscript.

Planned workflow:
- build the claim structure and paper outline first
- draft section-by-section with evidence discipline
- audit claims and citations before any submission packaging

Concrete outputs:
- survey outline
- full survey draft
- figure and table plan
- bibliography
- citation audit report

Recommended skill/agent routing:
- ARIS `paper-plan`
- ARIS `paper-write` or `paper-writing`
- ARIS `paper-figure`
- ARIS `paper-claim-audit`
- ARIS `citation-audit`
- `writer`

Exit criteria:
- survey draft is coherent, fully cited, and ready for venue-specific formatting

### Phase 4: Research Gap Extraction

Goal: convert the survey into a ranked agenda of high-value VLN research problems.

Planned workflow:
- extract unsolved problems directly from the survey evidence base
- filter out weak or already-saturated directions
- score ideas by novelty, feasibility, evaluation clarity, and CoRL fit

Concrete outputs:
- ranked gap list
- candidate problem statements
- risk log
- shortlist of method directions

Recommended skill/agent routing:
- `literature-reviewer`
- ARIS `idea-creator`
- ARIS `novelty-check`
- ARIS `research-review`

Exit criteria:
- one lead direction is chosen with a clear novelty thesis

### Phase 5: CoRL Method Planning

Goal: turn the selected gap into a research program before implementation.

Planned workflow:
- formalize the method hypothesis
- define baselines, datasets, metrics, ablations, and compute needs
- design failure-oriented sanity checks before major experiments

Concrete outputs:
- method hypothesis note
- experiment plan
- ablation plan
- resource budget
- submission timeline

Recommended skill/agent routing:
- ARIS `experiment-plan`
- ARIS `ablation-planner`
- `test-engineer` for evaluation coverage thinking
- `architect` for interface and system decomposition if code work becomes nontrivial

Exit criteria:
- experiment plan is concrete enough to execute on GPU resources

### Phase 6: CoRL Research Execution

Goal: implement, run, and iterate on the chosen method.

Planned workflow:
- implement the method conservatively
- run pilot experiments before full sweeps
- maintain result-to-claim discipline throughout iteration

Concrete outputs:
- reproducible implementation
- experiment logs
- audited results
- improvement loop records

Recommended skill/agent routing:
- `executor`
- ARIS `run-experiment`
- ARIS `monitor-experiment`
- ARIS `analyze-results`
- ARIS `result-to-claim`
- ARIS `auto-review-loop`

Exit criteria:
- the method has enough empirical support for paper writing

### Phase 7: CoRL Paper Production

Goal: produce a defensible CoRL submission package.

Planned workflow:
- write from verified claims only
- maintain an explicit evidence trail for each main contribution
- run final writing, claim, and citation audits

Concrete outputs:
- CoRL paper outline
- full draft
- figure set
- appendix plan
- citation and claim audit reports

Recommended skill/agent routing:
- ARIS `paper-plan`
- ARIS `paper-write` or `paper-writing`
- ARIS `paper-figure`
- ARIS `paper-claim-audit`
- ARIS `citation-audit`
- `rebuttal-writer` later if reviews arrive

Exit criteria:
- a submission-ready CoRL draft exists

## Execution Order

1. complete Phase 1 scoping
2. complete Phase 2 literature review
3. write the IEEE survey in Phase 3
4. only then move into Phase 4 gap extraction
5. do not start method implementation before Phase 5 is written down

## Quality Gates

- No paper should enter the core survey set without a documented reason.
- No major claim should survive without direct paper evidence.
- No new method direction should proceed without an explicit novelty check.
- No GPU experiment phase should start from the login node.
- No manuscript should be treated as ready before claim and citation audits complete.

## Immediate Next Step

When execution begins, the first real research action should be Phase 1 scoping:
- define the VLN scope boundary
- lock the taxonomy
- decide the literature inclusion policy

Until then, keep this repository in preparation mode only.
