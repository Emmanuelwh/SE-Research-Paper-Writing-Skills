# Methodology Examples

Use this file as the entry point for Methodology examples. Read `references/methodology.md` first, then open only the example that matches the current writing task.

## Tool Paper Examples

Use these for papers whose main contribution is a tool, analyzer, detector, repair technique, testing framework, auditing workflow, benchmarked pipeline, or LLM4SE system.

1. Tool overview and complete figure example: `references/examples/methodology/tool-overview-example.md`
2. Module subsection and step-level implementation example: `references/examples/methodology/module-subsection-example.md`

## Tool Paper Overview Mini-Pattern

`Given [input artifacts] from [SE task], [Tool] produces [final output] for [actor]. Figure X shows the workflow: [Module 1] transforms [input] into [artifact 1], [Module 2] derives [artifact 2], and [Module 3] generates [final output]. Sections X.1-X.3 describe these modules in the same order.`

## Tool Paper Module Mini-Pattern

`After [previous module] produces [artifact], the tool still needs to [remaining problem]. A direct approach based on [simple evidence] is insufficient because [reason]. To address this, we design [module], which [operation]. The module outputs [artifact], enabling [next module/final output].`

Technical-unit pattern:

`Given [input], [Tool] [operation] to produce [output]. During this process, [difficulty] arises because [reason]. To address this, [Tool] [design choice]. The resulting [artifact/state] is used by [next unit/module] to [purpose].`

## Empirical Study Examples

Use these for study-design Methodology sections.

### RQ Table Pattern

| RQ | Purpose | Data/Subjects | Analysis |
| --- | --- | --- | --- |
| RQ1 | Understand/measure [phenomenon] | [projects/participants/artifacts] | [statistics/coding/comparison] |
| RQ2 | Evaluate [method/tool] | [benchmark/tasks] | [metrics/baselines/tests] |

### Dataset Paragraph

`We selected [subjects] because they represent [scope]. We included [criteria] and excluded [criteria] to reduce [bias/noise]. The final dataset contains [scale], covering [languages/domains/time window].`

### Procedure Paragraph

`For each [unit], we first [step 1], then [step 2], and finally [step 3]. This procedure produces [output], which we use to measure [construct] for RQ[number].`

### Analysis Paragraph

`To answer RQ[number], we compare [groups/baselines] using [metric]. We report [statistical test/effect size/confidence interval] because [reason]. For qualitative data, two authors independently coded [sample] and resolved disagreements through discussion.`