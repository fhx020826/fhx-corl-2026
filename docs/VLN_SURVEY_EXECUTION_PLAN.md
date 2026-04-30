# VLN Survey Execution Plan

## Status

Preparation only. This plan defines how the VLN survey investigation should be executed after approval. It does not start literature collection.

## Goal

Build a comprehensive, low-bias VLN literature investigation that serves two purposes:

1. produce a publishable survey paper
2. build a field-level structural understanding that supports later method research

The primary execution target of this phase is a formal literature database of 100+ VLN-related papers, ordered by first arXiv submission date from newest to oldest, with strong coverage across all major sub-directions.

## Requirements Summary

- Start from existing VLN and embodied navigation survey papers.
- Analyze how prior surveys structure the field:
  - logic
  - taxonomy
  - categorization strategy
- Use the references cited in those surveys as the first expansion frontier.
- Expand beyond survey references using:
  - keyword search
  - arXiv
  - Google Scholar-style search surfaces
  - curated GitHub resources such as awesome-vln and similar maintained repositories
- Prioritize paper quality using:
  - citation strength
  - open-source ecosystem quality
  - maintained project pages
- Avoid bias toward a small subset of VLN methods or benchmarks.
- Do not start collection until this plan is approved.

## Deliverables

### Primary deliverables

1. `references/vln-survey-paper-list.md`
   - 100+ papers
   - title
   - first arXiv submission date
   - sorted reverse chronologically

2. `references/vln-survey-metadata.csv`
   - canonical machine-readable paper table

3. `docs/VLN_SURVEY_TAXONOMY.md`
   - taxonomy distilled from survey-of-surveys analysis

4. `docs/VLN_SURVEY_OF_SURVEYS.md`
   - structured analysis of existing survey papers

### Secondary deliverables

5. `references/vln-source-ledger.md`
   - provenance of every collected paper

6. `docs/VLN_COVERAGE_AUDIT.md`
   - explicit gap and bias audit

7. `survey-paper/outline.md`
   - survey manuscript outline after the taxonomy stabilizes

## Proposed File Structure

- `docs/VLN_SURVEY_EXECUTION_PLAN.md`
- `docs/VLN_SURVEY_OF_SURVEYS.md`
- `docs/VLN_SURVEY_TAXONOMY.md`
- `docs/VLN_COVERAGE_AUDIT.md`
- `references/vln-source-ledger.md`
- `references/vln-survey-paper-list.md`
- `references/vln-survey-metadata.csv`
- `survey-paper/outline.md`

## Execution Strategy

The execution should happen in seven stages.

### Stage 1: Survey-of-surveys scoping

Objective:
- find all directly relevant survey papers on VLN and the most relevant broader embodied navigation surveys

Main workflow:
- `literature-reviewer`
- ARIS-style `research-lit`
- `researcher` only for venue and metadata verification when needed

Actions:
- identify candidate survey papers
- separate them into:
  - VLN-specific surveys
  - broader embodied AI / embodied navigation surveys
  - tangential surveys that mention VLN but do not structure it meaningfully
- record for each survey:
  - scope
  - publication year
  - central taxonomy
  - main sections
  - what it excludes
  - what it over-emphasizes

Output:
- initial version of `docs/VLN_SURVEY_OF_SURVEYS.md`

Quality gate:
- do not move on until the survey set is broad enough to expose multiple competing ways of structuring the field

### Stage 2: Taxonomy extraction and synthesis

Objective:
- derive a robust taxonomy from prior surveys before expanding the paper list aggressively

Main workflow:
- `literature-reviewer`
- ARIS-style `research-review`
- `writer` for synthesis cleanup only after the technical structure is stable

Actions:
- compare survey taxonomies along multiple axes:
  - task formulation
  - environment type
  - instruction modality
  - embodiment assumptions
  - supervision level
  - perception and memory design
  - planning and policy structure
  - evaluation setting
  - benchmark lineage
- identify where prior surveys disagree
- produce a merged taxonomy that is broad enough for coverage control

Output:
- first stable version of `docs/VLN_SURVEY_TAXONOMY.md`

Quality gate:
- each major VLN sub-direction must have a clear bucket in the taxonomy

### Stage 3: Citation-seeded core expansion

Objective:
- use survey references as the initial high-signal seed set

Main workflow:
- `literature-reviewer`
- ARIS-style `research-lit`

Actions:
- extract all core references cited in the accepted survey set
- deduplicate titles across surveys
- mark paper provenance:
  - which survey cited it
  - how many surveys cited it
  - whether it appears as a foundational, benchmark, method, or systems paper
- assign preliminary taxonomy labels

Output:
- first population of `references/vln-survey-metadata.csv`
- provenance entries in `references/vln-source-ledger.md`

Quality gate:
- the seed set must cover classic and modern papers, not only recent popular models

### Stage 4: Multi-source frontier expansion

Objective:
- extend beyond survey citations to maximize coverage and reduce inherited bias from prior surveys

Main workflow:
- ARIS-style `research-lit`
- `literature-reviewer`

Sources to search:
- arXiv keyword search
- Google Scholar-style keyword search
- curated GitHub repositories such as awesome-vln
- project pages and benchmark pages discovered from seed papers

Search policy:
- build multiple query families instead of a single keyword list
- include both direct VLN and neighboring embodied navigation wording
- include task, benchmark, and method-centric phrases

Query families:
- direct VLN terms
- embodied instruction-following navigation
- vision-language embodied agents
- indoor VLN and outdoor VLN
- simulator and real-world VLN
- long-horizon instruction following
- map-based, memory-based, transformer-based, and foundation-model-based VLN
- multilingual or dialogue-based navigation where relevant

Output:
- expanded paper inventory

Quality gate:
- no major taxonomy branch should depend on only one source channel

### Stage 5: Quality ranking without exclusion bias

Objective:
- prioritize high-quality papers while preserving broad field coverage

Main workflow:
- `literature-reviewer`
- ARIS-style `research-review`

Actions:
- add quality signals for each paper:
  - citation strength
  - code availability
  - repository activity
  - project page availability
  - benchmark influence
- separate:
  - coverage inclusion
  - high-priority reading
- avoid dropping lower-citation but structurally important papers if they define a sub-direction

Output:
- quality annotations inside `references/vln-survey-metadata.csv`

Quality gate:
- strong papers should be prioritized, but the final list must still represent the field rather than just the citation elite

### Stage 6: Coverage and bias audit

Objective:
- explicitly test whether the collected set is balanced across the taxonomy

Main workflow:
- `literature-reviewer`
- ARIS-style `research-review`
- `critic` if the field coverage looks skewed

Actions:
- count papers per taxonomy branch
- identify overrepresented branches
- identify underrepresented branches
- inspect whether the search process is biased toward:
  - only high-citation classics
  - only recent LLM-era papers
  - only indoor benchmarks
  - only a narrow benchmark ecosystem
  - only papers with code
- run targeted backfill searches for weak branches

Output:
- `docs/VLN_COVERAGE_AUDIT.md`

Quality gate:
- proceed only when the paper set has acceptable branch coverage and the missing zones are explicitly documented

### Stage 7: Finalization of the formal paper list

Objective:
- freeze the formal deliverable list and make it publication-ready

Main workflow:
- `writer`
- `verifier`

Actions:
- verify every title
- verify every first arXiv submission date
- sort reverse chronologically by first arXiv submission date
- ensure deterministic formatting
- keep machine-readable and human-readable lists synchronized

Output:
- final `references/vln-survey-paper-list.md`
- final `references/vln-survey-metadata.csv`

Quality gate:
- 100+ papers
- ordering verified
- metadata spot-checked

## Inclusion Policy

Include papers that satisfy at least one of the following:

- direct VLN task papers
- core benchmark papers that shaped VLN evaluation
- broader embodied navigation papers that materially structure VLN methods or survey framing
- adjacent embodied instruction-following papers that are necessary to explain the field boundary

Exclude or mark separately:

- papers with only passing VLN mention and no structural relevance
- purely unrelated embodied AI work
- duplicate versions where the canonical arXiv record is already captured

## Taxonomy Policy

The taxonomy should not assume one dominant lens. It should support parallel views.

Required taxonomy views:
- chronological view
- task-setting view
- method-family view
- supervision and data view
- benchmark and evaluation view
- embodiment and deployment view

This is necessary to avoid a paper list that overfits one survey logic.

## Source Provenance Policy

Every paper should record at least one provenance tag:

- `survey-citation`
- `keyword-search`
- `arxiv-search`
- `scholar-search`
- `awesome-repo`
- `project-page`
- `backfill-search`

This is required for auditing where the collection is coming from.

## Ranking Policy

Maintain two distinct labels:

1. `coverage-core`
   - included because it is necessary for broad field coverage

2. `priority-core`
   - included and prioritized because it is also highly influential or well-supported by ecosystem quality

This prevents high-citation preference from collapsing the scope.

## Acceptance Criteria

- A survey-first plan exists before any collection begins.
- Existing VLN and embodied navigation surveys are analyzed before broad search starts.
- The taxonomy is derived before the paper list becomes large.
- The final paper database contains at least 100 papers.
- The final list contains title and first arXiv submission date for each paper.
- The final list is sorted from newest to oldest by first arXiv submission date.
- Source provenance exists for every paper.
- Coverage is audited against an explicit taxonomy.
- The collection process includes targeted backfill for under-covered branches.
- High-quality papers are prioritized, but not at the cost of structural coverage.

## Risks and Mitigations

### Risk 1: inherited bias from prior surveys

Mitigation:
- treat surveys as seeds, not as the whole field
- force Stage 4 multi-source expansion
- run Stage 6 coverage audit

### Risk 2: overconcentration on popular benchmarks

Mitigation:
- taxonomy must include benchmark lineage explicitly
- run backfill searches centered on underrepresented settings

### Risk 3: recent-paper bias

Mitigation:
- separate chronological sorting from inclusion logic
- preserve foundational papers even when older and less visible in current search surfaces

### Risk 4: citation-count bias

Mitigation:
- use quality ranking only after inclusion
- preserve lower-citation but structurally important papers

### Risk 5: metadata inconsistency for arXiv dates

Mitigation:
- define one canonical rule: first arXiv submission date
- verify at finalization stage with spot checks

## Verification Plan

Before execution begins:
- review this plan for scope completeness
- verify that the deliverables and file structure are acceptable

During execution:
- checkpoint after Stage 1 with the survey-of-surveys set
- checkpoint after Stage 2 with the taxonomy
- checkpoint after Stage 4 when the inventory reaches roughly 60 to 80 papers
- checkpoint after Stage 6 before freezing the final 100+ list

At completion:
- verify count >= 100
- verify chronological sorting
- verify provenance coverage
- verify taxonomy branch coverage

## Recommended Skill and Agent Routing

Primary stack for this task:
- `literature-reviewer`
- ARIS-style `research-lit`
- ARIS-style `research-review`

Secondary stack:
- `researcher`
- `writer`
- `critic`
- `verifier`

Suggested role split when execution starts:
- `literature-reviewer`: survey-of-surveys and core search logic
- `researcher`: targeted metadata and venue verification
- `writer`: synthesis cleanup and deliverable formatting
- `critic`: anti-bias review of taxonomy and coverage
- `verifier`: final sort and metadata checks

## Recommended Execution Order After Approval

1. execute Stage 1 and produce the survey-of-surveys note
2. execute Stage 2 and freeze the first taxonomy
3. execute Stage 3 and Stage 4 to build the inventory
4. execute Stage 5 and Stage 6 to audit quality and coverage
5. execute Stage 7 to freeze the formal paper list

## Explicit Non-Goals for This Phase

- do not write the full survey manuscript yet
- do not design a new VLN method yet
- do not run experiments
- do not claim field coverage until the bias audit is complete
