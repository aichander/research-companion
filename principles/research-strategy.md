# Research Strategy Principles (8)

Derived from patterns observed in high-impact research. These principles guide strategic thinking about *what* to work on and *how* to evaluate research directions — the decisions that happen before writing begins.

Reference: Nicholas Carlini, ["How to Win a Best Paper Award"](https://nicholas.carlini.com/writing/2026/how-to-win-a-best-paper-award.html)

---

## A. Problem Selection

### RS1: The Novelty Test

**"If you don't do this, how many months until someone else does?"**

The magnitude of your contribution correlates with the gap between your publication and when someone else would independently achieve similar results. If the answer is "a few weeks," the idea may not be worth months of effort — you're in a race you might lose, and even winning yields only incremental credit.

**Apply when:** Evaluating whether to start a new project. Favor problems where your unique combination of skills, knowledge, or perspective creates a gap of months or years, not weeks.

### RS2: The Conclusion-First Test

**"Can you write a compelling conclusion right now, without doing the work?"**

Before investing in research, write the best-case conclusion. If you cannot articulate why the work matters beyond "our method improved numbers by X%," the project may lack sufficient impact to justify the effort.

**Apply when:** Starting a new project, or at a go/no-go decision point. If the conclusion writes itself and feels important, proceed. If it feels hollow or generic, reconsider.

### RS3: The Nugget Test

**"Can you state the key insight in one sentence?"**

Every strong paper advances exactly one idea expressible in a few words. If you cannot state it, the idea is either too vague, too diffuse, or not yet crystallized. Multiple ideas dilute the message — readers remember none when forced to choose among many.

**Apply when:** Before outlining or drafting. Write the nugget down and keep it visible throughout the project. Every experiment and figure should connect to it.

---

## B. Execution Strategy

### RS4: Fail Fast

**"Start with the sub-problem most likely to kill the project."**

Most ideas die upon contact with reality. Minimize wasted time by identifying and testing the riskiest assumption first. Build small prototypes to validate core feasibility before investing in polish, scale, or completeness.

**Apply when:** Planning experiments. Order your work by risk, not by logical sequence or ease. If the hardest part doesn't work, nothing else matters.

### RS5: Kill Early

**"A working project with low impact is worse than a killed project."**

Technical contributions may exist and results may trend positive, but if the paper lacks potential impact, terminate it. Sunk cost is not a reason to continue. Convert to a workshop paper or blog post if the work has some value, but don't pursue a full paper that will be forgettable.

**Apply when:** Mid-project check-ins. Ask: "If this works perfectly, will anyone care?" If the honest answer is "not really," cut your losses.

### RS6: Unreasonable Effort

**"Strengthen 'sometimes' to 'usually' through additional work."**

Beyond having good ideas and skill, great papers result from effort exceeding reasonable expectations. Run additional trials, control confounders, anticipate skeptical reader questions and answer them preemptively. The difference between a good paper and a great one is often the willingness to do work others would consider excessive.

**Apply when:** Once a project has passed the kill tests and you're committed. This principle applies *after* RS4 and RS5 — unreasonable effort on the wrong project is still wasted effort.

---

## C. Strategic Positioning

### RS7: Comparative Advantage

**"Research space is high-dimensional; find your unique corner."**

You are almost certainly world-best at some specific combination of skills, knowledge, and perspective. Identify that corner and work in it. Being first in a young field carries outsized impact. Bridging distant fields (e.g., connecting cryptanalysis to model stealing, or semi-supervised learning to poisoning attacks) creates contributions that researchers in either field alone would not produce.

**Apply when:** Choosing between research directions. Favor directions where your specific skill combination creates an unfair advantage, and where competitors are unlikely to arrive soon.

### RS8: Timing Awareness

**"Impact = skill in domain × importance of domain at this moment."**

You control your skill but not when the world needs it. Problems vary in importance depending on the current state of scientific knowledge and practical deployment. Being too early means reviewers reject your premises; being too late means the contribution is incremental. Truly impactful researchers sense when their skills align with emerging importance — and pivot when that alignment shifts.

**Apply when:** Evaluating research directions at a strategic level. Monitor which problems are becoming more important (not just which are currently popular). Consider whether your current focus area is gaining or losing relevance.

---

## D. Biology-Specific Principles

### RS9: Open Science Value

**"Will this generate a community resource — data, atlas, tool, or protocol — that enables research beyond your own lab?"**

In biology, the highest-impact contributions are often not individual mechanistic findings but infrastructure: reference atlases, openly shared datasets, validated reagent panels, computational pipelines. A single-cell atlas used by 500 downstream labs may have more total impact than 50 papers. This is especially true at the scale of projects like the Allen Brain Atlas, Human Cell Atlas, or ImmPort.

**Apply when:** Evaluating whether to invest in large-scale data generation. Ask: if this dataset were made publicly available, how many research questions could it unlock that aren't currently answerable? If the answer is "many," the open science value may justify the project even if your own mechanistic question is narrow.

### RS10: Experimental Rigor Path

**"What is the minimum valid experiment? Can you answer this with existing public data before committing wet lab resources?"**

Biology's timelines are unforgiving — a single experiment can take weeks or months, and a poorly designed one yields ambiguous results. Before designing a new experiment, audit what already exists: public databases (Allen Brain Atlas, Human Cell Atlas, GEO, ImmPort, ENCODE, GTEx, UK Biobank, CZI CELLxGENE) may already contain the data needed to validate or kill the core assumption. When wet lab work is required, identify the riskiest assumption first (RS4) and design the smallest experiment that tests it with adequate statistical power — accounting for biological variance, not just technical variance.

**Apply when:** Designing experiments or evaluating proposals. Flag when a study lacks power analysis accounting for donor-to-donor or sample-to-sample variability. Flag when expensive new data generation is proposed without first checking existing public resources.

### RS11: Model System Validity

**"Does the model system support the biological claim at the right level of complexity?"**

Biology is full of findings that replicate beautifully in cell lines, fail in primary cells, and vanish in vivo. Every model system — immortalized cell line, primary culture, organoid, mouse model, non-human primate, human tissue — makes tradeoffs between tractability and biological fidelity. A claim about human immune function derived entirely from mouse knockouts should be held to a different standard than one validated in primary human tissue. A neural circuit finding in an acute slice preparation may not hold in the intact behaving animal.

**Apply when:** Evaluating the scope of any biological claim. Ask: what is the most complex or physiologically relevant system in which this has been tested? What would change if the experiment were done one level up in complexity? Is the gap between the model system used and the system the claim is about acknowledged and addressed?
