# Research Companion — Biology Edition

**Strategic research thinking agents for [Claude Code](https://docs.anthropic.com/en/docs/claude-code)** — idea evaluation, project triage, structured brainstorming, and adversarial critique of manuscripts, grants, and proposals.

Tuned for **immunology, neuroscience, cell science, and neural dynamics** — with strong emphasis on cross-field connections from physics, engineering, math, CS, and economics, and a dedicated computational methods advisor for large biology datasets.

Most AI writing tools help you *write* papers. This plugin helps you decide *which* papers to write — and finds the holes in what you've already written.

Inspired by Nicholas Carlini's essay ["How to Win a Best Paper Award"](https://nicholas.carlini.com/writing/2026/how-to-win-a-best-paper-award.html)

Original Skill by [Haiwen Huang](https://github.com/andrehuang/research-companion)

## The Problem

Researchers don't lack the ability to write papers. They lack a trusted colleague who will:

- Tell them an idea isn't worth 6 months of their life — *before* they invest those months
- Ask "who else is working on this and what's your unfair advantage?"
- Challenge them to state the key insight in one sentence (and refuse to move on until they can)
- Help them find the unexpected cross-field connection that makes a contribution truly novel
- Evaluate whether a struggling project should be continued, pivoted, or killed

This plugin provides that colleague.

## Installation

`claude plugin install https://github.com/aichander/research-companion.git`

Or from a locally cloned folder:
`claude plugin install /path/to/research-companion`

That's it. The /research-companion skill and all agents are immediately
available in any Claude Code session.


## What's Inside

### Agents

| Agent | What it does |
|-------|-------------|
| **Idea Critic** | Stress-tests research ideas along 8 dimensions: novelty, impact, timing, feasibility, competitive landscape, the nugget, narrative potential, and experimental design & data availability. Returns a Pursue / Refine / Kill verdict. |
| **Research Strategist** | Project-level strategic thinking — triage (continue/pivot/kill), comparative advantage mapping, impact forecasting, opportunity cost analysis, scooping risk assessment, and experimental design & data strategy. |
| **Brainstormer** | Creative brainstormer with explicit focus on cross-field connections from distant domains (physics, engineering, CS, math, economics, ecology), challenging flawed biological assumptions, and the skeptical-reader test. |
| **Document Critic** | Adversarial critique of manuscripts, grants, and proposals — finds gaps, missing controls, overclaiming, model system issues, and surfaces computational methods from other fields that could extract more from your data. |

### Skill

| Skill | What it does |
|-------|-------------|
| `/research-companion` | A structured multi-phase session that orchestrates all agents. Accepts a research topic/hypothesis **or** a document (manuscript, grant, proposal) and routes accordingly. |

### Principles

11 research strategy principles organized into four categories (Problem Selection, Execution Strategy, Strategic Positioning, Biology-Specific) that guide the agents' evaluations.

## Usage

### Evaluate a research idea

Just describe your idea and ask for evaluation:

```
Is it interesting to study clonal dynamics of B cells in tumor-adjacent tissue?
Why should we invest in building a single-cell atlas of the human thymus?
Has anyone mapped astrocyte subtypes in the aging human brain with spatial transcriptomics?
```

The **Idea Critic** will evaluate across 8 dimensions and give you a verdict with the single most important question to resolve next.

### Decide whether to continue a project

```
I've been working on characterizing microglia states in neurodegeneration for 3 months.
I have some results but another group just posted a preprint in the same area.
Should I continue?
```

The **Research Strategist** will assess your competitive position, impact potential, opportunity cost, and recommend Continue / Pivot / Kill — including what public data already exists and what experiment to run next.

### Critique a manuscript, grant, or proposal

```
/research-companion [paste abstract, specific aims, or give a file path]
```

The **Document Critic** will find gaps, missing controls, overclaiming, model system issues, and — critically — identify computational methods from other fields (optimal transport, causal inference, topological data analysis, tensor decomposition, control theory) that could extract substantially more from the data described.

### Run a full brainstorming session

```
/research-companion I'm interested in how tissue-resident immune cells in the brain
respond differently to neuroinflammation than circulating immune cells
```

This launches a 6-phase guided session:

1. **Seed** — Understand your problem space, background, data access, and what bugs you about the field
2. **Diverge** — Generate ideas and cross-field connections (from physics, engineering, CS, math — not just adjacent biology)
3. **Evaluate** — Stress-test the top 2-3 ideas with the Idea Critic
4. **Deepen** — Check novelty, positioning, competitive landscape, and experimental design
5. **Frame** — Write the abstract and conclusion as if the paper is done (the conclusion-first test: if you can't write a compelling conclusion now, the idea isn't ready)
6. **Decide** — Final assessment with next steps (starting with the single riskiest assumption to test first)

## The 8 Evaluation Dimensions

When the Idea Critic evaluates your research idea, it assesses:

| # | Dimension | Key Question |
|---|-----------|-------------|
| 1 | **Novelty** | If you don't do this, how long until someone else does? |
| 2 | **Impact** | Can you write a compelling conclusion *right now*, without doing the work? |
| 3 | **Timing** | Is the field ready for this? Too early? Already crowded? |
| 4 | **Feasibility** | What's the riskiest assumption? Can you test it with existing public data first? |
| 5 | **Competitive Landscape** | Who else is working on this? What's your unfair advantage? |
| 6 | **The Nugget** | Can you state the key insight in one sentence? |
| 7 | **Narrative Potential** | Can you tell a story that makes a skeptical reader care? |
| 8 | **Experimental Design & Data** | Is there existing public data? Is the model system right? Is the study powered for biological variance? |

## The 11 Research Strategy Principles

These principles, derived from patterns in high-impact research, guide all agents in this plugin:

**Problem Selection**
- **RS1: The Novelty Test** — "If you don't do this, how many months until someone else does?"
- **RS2: The Conclusion-First Test** — "Can you write a compelling conclusion right now?"
- **RS3: The Nugget Test** — "Can you state the key insight in one sentence?"

**Execution Strategy**
- **RS4: Fail Fast** — "Start with the sub-problem most likely to kill the project"
- **RS5: Kill Early** — "A working project with low impact is worse than a killed project"
- **RS6: Unreasonable Effort** — "Strengthen 'sometimes' to 'usually' through additional work"

**Strategic Positioning**
- **RS7: Comparative Advantage** — "Research space is high-dimensional; find your unique corner"
- **RS8: Timing Awareness** — "Impact = skill × domain importance at this moment"

**Biology-Specific**
- **RS9: Open Science Value** — "Will this generate a community resource (atlas, dataset, tool) that enables downstream research for others?"
- **RS10: Experimental Rigor Path** — "Check public data first before committing wet lab resources; design for biological variance, not just technical variance"
- **RS11: Model System Validity** — "Does the model system (cell line, mouse, organoid, human tissue) actually support the claim being made?"

## Persistent Evaluations (NEW in v1.1)

Evaluation results are now **saved to disk** so they persist across sessions:

- After each session, verdicts are written to `research-evaluations/YYYY-MM-DD-<topic>.md`
- On subsequent sessions, the system **checks for prior evaluations** of similar topics before starting fresh
- PARK'd ideas include "revisit conditions" — what would need to change to reconsider
- The Research Strategist now outputs a **watch list** (search terms, key researchers, venues to monitor) for competitive tracking
- The Idea Critic checks for prior evaluations to avoid re-evaluating killed ideas unless conditions have changed

This means your research thinking accumulates over time rather than starting from scratch each session.

## Pairs Well With

- [**Academic Writing Agents**](https://github.com/andrehuang/academic-writing-agents) — 12 agents for reviewing, auditing, drafting, and polishing academic papers. Research Companion handles the "what to write" question; Academic Writing Agents handles the "how to write it" question.
- [**Claude-Claw**](https://github.com/andrehuang/claude-claw) — OpenClaw-inspired enhancements for session continuity, task management, and memory architecture. Provides `/handoff` for saving session state and `/manager` for tracking research tasks.

## Philosophy

Most researchers optimize for publication count. The best researchers optimize for impact — and papers follow naturally. This plugin is built around that distinction.

It won't help you produce more papers. It will help you produce *better* ones by being honest about which ideas are worth your finite time and by stress-testing your thinking before you commit months of effort.

The agents are deliberately opinionated and direct. They'd rather save you 3 months than spare your feelings. If an idea should be killed, they'll say so — and explain why.

## License

MIT
