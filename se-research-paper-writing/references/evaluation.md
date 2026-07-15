# Evaluation Writing Guide

## Goal

Write Evaluation so reviewers can see that the evidence answers the RQs, supports the contribution claims, and honestly communicates limitations.

## Evaluation Planning

For each RQ, define:

1. Claim being tested.
2. Dataset/subjects/tasks.
3. Baselines or comparison groups.
4. Metrics and why they matter.
5. Analysis method.
6. Expected table/figure.
7. Threats and mitigation.

## Common Evaluation Components

### Experimental Setup

Describe hardware/software environment, tool versions, model versions, datasets, project selection, task construction, time windows, and replication package.

### Main Results

Answer each RQ directly. Start with the takeaway, then provide evidence, then interpret the result.

### Comparison Against Baselines

Use baselines that represent current practice, recent research, simple heuristics, and ablated variants when applicable. Explain why each baseline is fair.

### Ablation or Sensitivity Analysis

Use when the paper makes design claims. Show which component, prompt, heuristic, data source, or algorithmic choice contributes to the result.

### Qualitative Analysis

Use when numbers alone cannot explain behavior. Report coding process, examples, categories, and disagreement resolution.

### Failure Cases

Include failure modes when they teach reviewers the boundary of the contribution. Tie failure cases to threats and future work.

## Result Paragraph Pattern

1. Takeaway: answer the RQ in one sentence.
2. Evidence: cite table/figure and key numbers or qualitative categories.
3. Interpretation: explain why the result matters for the SE problem.
4. Boundary: state when the result may not hold.

## Table and Figure Rules

1. One table or figure should communicate one message.
2. Label metric direction and units.
3. Keep numeric precision consistent.
4. Put statistical significance and effect size near the relevant metric.
5. Use captions to state setting, subjects, and notation, not long discussion.
6. Avoid hiding negative or insignificant results.

## Checklist

1. Does every RQ receive a direct answer?
2. Are baselines strong, recent, and fair?
3. Are metrics valid for the SE construct?
4. Are statistical tests and effect sizes reported when needed?
5. Are practical implications separated from statistical significance?
6. Are negative results and failure cases handled honestly?
7. Are all Abstract/Introduction claims supported by Evaluation evidence?
