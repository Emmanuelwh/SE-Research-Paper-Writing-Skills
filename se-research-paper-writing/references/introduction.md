# Introduction Writing Guide

## Goal

Write an Introduction that convinces SE reviewers that the problem matters, the gap is real, the contribution is specific, and the evidence plan can support the claims.

## Introduction Logic Map

1. SE context: identify the software engineering activity, stakeholder, and consequence.
2. Problem: explain what is difficult, costly, error-prone, understudied, or unsupported.
3. Prior work/current practice: summarize what exists and why it is insufficient.
4. Gap: state the precise missing knowledge, capability, benchmark, tool support, or methodological limitation.
5. Insight: explain the key observation that enables the paper's contribution.
6. Contribution: present artifact/study/method/dataset/taxonomy with clear boundaries.
7. Evidence: preview methodology and evaluation at the right level of detail.
8. Implication: explain what the results change for researchers or practitioners.

## Section Skeleton

1. Paragraph 1: SE setting and why the problem matters.
2. Paragraph 2: concrete challenge and limitation of current approaches.
3. Paragraph 3: paper insight or opportunity.
4. Paragraph 4: proposed study/method/tool and contribution summary.
5. Paragraph 5: evaluation evidence and main results.
6. Paragraph 6: contributions list.

## Contribution Framing

Use contribution bullets only after the story has made them necessary. Good contribution bullets are specific and evidence-aware:

1. `We formulate ...` for new problem definitions, taxonomies, or benchmarks.
2. `We design and implement ...` for tools and systems.
3. `We conduct ...` for empirical studies, controlled experiments, interviews, surveys, or mixed-methods studies.
4. `We provide evidence that ...` for findings supported by evaluation.
5. `We release ...` for datasets, artifacts, replication packages, or benchmarks.

Avoid contribution bullets that only say `We propose a novel approach` without naming what is new and why it matters.

## SE-Specific Checks

1. Is the problem anchored in a real SE workflow?
2. Does the gap follow from prior work rather than from the authors' preference?
3. Are RQs or evaluation goals foreshadowed before results appear?
4. Are claims scoped to the studied languages, projects, tasks, or participants?
5. Does the introduction explain why the paper belongs in a software engineering venue?

## Common Failure Modes

1. Starting with broad software importance but never naming the concrete SE pain point.
2. Treating a model/tool improvement as self-evidently useful without explaining the workflow impact.
3. Listing prior work without articulating the missing capability or knowledge gap.
4. Claiming generality before describing the empirical scope.
5. Reporting results in the introduction that are not traceable to later tables or figures.
