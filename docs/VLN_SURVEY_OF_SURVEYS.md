# VLN Survey of Surveys

## Purpose

This note completes Stage 1 of the VLN survey workflow at an initial level:

- identify existing VLN-specific and broader embodied-navigation surveys
- compare how they organize the field
- decide which surveys are reliable seed sources for the later paper inventory

This document is intentionally pre-taxonomy. It analyzes prior organizing strategies without committing to our own final classification scheme.

## Survey Set

### A. Core VLN-specific surveys

1. **Vision-Language Navigation: A Survey and Taxonomy**
   - Authors: Wansen Wu, Tao Chang, Xinmeng Li
   - First arXiv submission: 2021-08-26
   - URL: https://arxiv.org/abs/2108.11544
   - Role in our workflow: primary seed survey

2. **Vision-and-Language Navigation: A Survey of Tasks, Methods, and Future Directions**
   - Authors: Jing Gu, Eliana Stefani, Qi Wu, Jesse Thomason, Xin Eric Wang
   - First arXiv submission: 2022-03-22
   - URLs:
     - https://arxiv.org/abs/2203.12667
     - https://aclanthology.org/2022.acl-long.524/
   - Role in our workflow: primary seed survey

3. **Visual language navigation: a survey and open challenges**
   - Authors: Sang Min Park, Young Gab Kim
   - Published online: 2022-03-25
   - Journal issue date: January 2023
   - arXiv status: no confirmed arXiv preprint found yet
   - URL: https://doi.org/10.1007/s10462-022-10174-9
   - Role in our workflow: primary seed survey

4. **Vision-Language Navigation with Embodied Intelligence: A Survey**
   - Authors: Peng Gao, Peng Wang, Feng Gao, Fei Wang, Ruyue Yuan
   - First arXiv submission: 2024-02-22
   - URL: https://arxiv.org/abs/2402.14304
   - Status: withdrawn
   - Role in our workflow: contextual only, not a trusted seed source

5. **Vision-and-Language Navigation Today and Tomorrow: A Survey in the Era of Foundation Models**
   - Authors: Yue Zhang, Ziqiao Ma, Jialu Li, Yanyuan Qiao, Zun Wang, Joyce Chai, Qi Wu, Mohit Bansal, Parisa Kordjamshidi
   - First arXiv submission: 2024-07-09
   - URL: https://arxiv.org/abs/2407.07035
   - Role in our workflow: primary seed survey, especially for recent foundation-model-era papers

6. **A comprehensive review of recent advancements in vision-and-language navigation**
   - Published: 2026-03-21
   - arXiv status: no confirmed arXiv preprint found yet
   - URL: https://link.springer.com/article/10.1007/s10791-026-09977-z
   - Role in our workflow: secondary seed survey, useful for recent coverage and real-world deployment discussion

### B. Broader embodied-navigation / embodied-AI surveys

7. **A Survey of Embodied AI: From Simulators to Research Tasks**
   - Authors: Jiafei Duan, Samson Yu, Hui Li Tan, Hongyuan Zhu, Cheston Tan
   - First arXiv submission: 2021-03-08
   - URL: https://arxiv.org/abs/2103.04918
   - Role in our workflow: contextual boundary survey

8. **Foundation Models for Embodied Navigation: A Survey**
   - Project page: https://membodied.github.io/embodied-navigation-survey/
   - PDF: https://membodied.github.io/embodied-navigation-survey/static/pdfs/foundation-models-for-embodied-navigation-a-survey.pdf
   - Dated on PDF front page: 2026-03-25
   - Role in our workflow: contextual boundary survey with strong value for post-LLM embodied navigation framing

## Reliability Assessment for Seeding the Later Paper Inventory

### Trusted primary seed surveys

- `Wu et al. 2021`
- `Gu et al. 2022`
- `Park and Kim 2023`
- `Zhang et al. 2024`

These four are the strongest starting points because they are directly about VLN and expose clearly different organizing logics.

### Trusted secondary seed surveys

- `Khan et al. 2026` review
- `Gao et al. 2026` embodied-navigation foundation-model survey
- `Duan et al. 2021` embodied AI survey

These are useful for expanding coverage beyond the classic indoor VLN literature and for identifying neighboring embodied navigation work that may otherwise be missed.

### Caution / do not trust as a seed authority

- `Gao et al. 2024`, **Vision-Language Navigation with Embodied Intelligence: A Survey**

Reason:
- the arXiv record states that the paper was withdrawn
- the withdrawal note explicitly mentions unauthorized figure usage and improper citation in a table

We may still inspect it for hints about what topics people try to group together, but we should not use it as an authoritative source when building the formal paper database.

## How Existing Surveys Organize the Field

### 1. Wu et al. 2021: instruction-structure-first taxonomy

Main logic:
- classify VLN tasks by the **characteristics of language interaction**

Top-level structure from the abstract:
- single-turn tasks
- multi-turn tasks

Further subdivision:
- single-turn:
  - goal-oriented
  - route-oriented
- multi-turn:
  - passive
  - interactive

Observed strengths:
- clear and compact
- grounded in human-agent communication structure
- useful for distinguishing classical instruction following from dialog-heavy settings

Observed limitations:
- the organizing principle is strongly instruction-centric
- method families, deployment setting, embodiment, and benchmark ecosystem are secondary
- some modern foundation-model and real-world continuous-control work does not fit cleanly into this lens alone

### 2. Gu et al. 2022: benchmark-and-challenge-driven organization

Main logic:
- jointly organize the field by **task setting** and **agent challenge**

Key evidence:
- they explicitly categorize benchmarks by `Communication Complexity` and `Task Objective`
- they categorize solution methods by challenge classes:
  - representation learning
  - action strategy learning
  - data-centric learning
  - prior exploration

What this means structurally:
- tasks/datasets are organized with one scheme
- methods are organized with another scheme
- the survey is less a single taxonomy and more a layered analytical map

Observed strengths:
- practical for a field survey
- makes the benchmark-method relationship explicit
- captures why different papers exist, not just what dialogue form they use

Observed limitations:
- not a single consistent partition of the whole field
- methods are grouped by problem-solving function rather than one unified scientific criterion
- useful for review writing, but weaker as a canonical taxonomy

### 3. Park and Kim 2023: technique-centric four-perspective survey

Main logic:
- analyze VLN from **four technical perspectives**

Explicit perspectives from the abstract:
- representation learning
- reinforcement learning
- component
- evaluation

Observed strengths:
- method-focused and systems-oriented
- useful for surveying model design choices and technical bottlenecks
- surfaces core engineering issues such as multimodal integration and data scarcity

Observed limitations:
- the categories are not mutually exclusive in a strict sense
- more of a review framework than a clean task taxonomy
- strong for method analysis, weaker for coverage control across datasets, deployment regimes, and embodiment settings

### 4. Zhang et al. 2024: top-down planning-and-reasoning framework

Main logic:
- organize VLN through a **principled embodied planning framework**

Key evidence from the HTML version:
- the survey is structured around:
  - `World Model`
  - `Human Model`
  - `VLN Agent`
- background material covers:
  - task formulations
  - benchmarks
  - evaluation metrics
  - foundation models
- future directions are also aligned to the same decomposition:
  - benchmarks
  - world model
  - human model
  - agent model
  - deployment

Observed strengths:
- the most coherent high-level conceptual structure among the VLN-specific surveys we inspected
- naturally accommodates foundation models, planning, memory, ambiguity, reasoning, and deployment
- useful for connecting classical VLN with the foundation-model era

Observed limitations:
- optimized for the foundation-model framing
- may overweight planning/reasoning abstractions relative to older benchmark-centric papers
- still not a neutral corpus-wide taxonomy by itself

### 5. Khan et al. 2026: unified synthesis from foundations to deployment

Main logic:
- present a **unified progression** from conceptual foundations to real-world deployment

Observed emphasis:
- practical robotic deployment
- sim-to-real gap
- continuous navigation
- real-world validation

Observed value for us:
- useful as a late-stage coverage checker for recent work
- especially helpful for identifying papers that a simulator-centric survey might underweight

### 6. Duan et al. 2021 and Gao et al. 2026: boundary-setting embodied surveys

Main logic:
- VLN is treated as part of a wider embodied-navigation or embodied-AI landscape

Useful boundary contribution:
- they remind us not to reduce VLN to only R2R-style indoor instruction following
- they broaden the neighboring search space toward:
  - simulators
  - visual navigation
  - deployment
  - embodiment-specific constraints
  - non-VLN embodied navigation families that may still matter for survey positioning

Risk if overused:
- these broader surveys can dilute the VLN core if used uncritically

## Cross-Survey Comparison

### What differs most across surveys

1. **Primary organizing lens**
- Wu et al. 2021: instruction interaction structure
- Gu et al. 2022: benchmarks plus challenge-oriented methods
- Park and Kim 2023: technical perspectives
- Zhang et al. 2024: embodied planning/reasoning architecture

2. **Scope boundary**
- some surveys stay close to canonical VLN benchmarks
- others extend toward dialog, object interaction, embodied QA, or broader embodied navigation

3. **Treatment of methods**
- some use challenge categories
- some use architectural categories
- some emphasize task or instruction form more than method family

4. **Treatment of deployment**
- earlier surveys are more benchmark-centric
- newer surveys increasingly foreground real-world deployment and foundation models

## Initial Conclusions for Our Own Workflow

### What we should copy

- from `Wu et al. 2021`: the discipline of defining task forms explicitly
- from `Gu et al. 2022`: the separation between task structure and method structure
- from `Park and Kim 2023`: the usefulness of perspective-based technical analysis
- from `Zhang et al. 2024`: the value of a top-down organizing principle that connects tasks, reasoning, memory, and planning
- from broader embodied surveys: the reminder to include deployment and embodiment boundaries

### What we should avoid

- locking into a taxonomy before corpus coverage is broad enough
- inheriting only one survey’s logic as if it were the field itself
- overfitting the paper inventory to indoor benchmark lineages
- using a withdrawn survey as an authoritative citation seed

## Stage-1 Decision

For Stage 2 onward, the initial trusted seed surveys are:

- Wu et al. 2021
- Gu et al. 2022
- Park and Kim 2023
- Zhang et al. 2024

The following will be used as secondary coverage expanders:

- Duan et al. 2021
- Khan et al. 2026
- Gao et al. 2026

The withdrawn survey `arXiv:2402.14304` is excluded from trusted seeding.

## Sources

- Wu et al. 2021 arXiv: https://arxiv.org/abs/2108.11544
- Gu et al. 2022 ACL: https://aclanthology.org/2022.acl-long.524/
- Gu et al. 2022 arXiv: https://arxiv.org/abs/2203.12667
- Park and Kim 2023: https://doi.org/10.1007/s10462-022-10174-9
- Gao et al. 2024 withdrawn survey: https://arxiv.org/abs/2402.14304
- Zhang et al. 2024: https://arxiv.org/abs/2407.07035
- Duan et al. 2021: https://arxiv.org/abs/2103.04918
- Gao et al. 2026 embodied navigation survey page: https://membodied.github.io/embodied-navigation-survey/
- Khan et al. 2026 review: https://link.springer.com/article/10.1007/s10791-026-09977-z
