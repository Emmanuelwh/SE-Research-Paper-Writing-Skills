# Evaluation Writing Guide

## Goal

Write Evaluation so reviewers can see exactly how the paper tests its claims. Always begin with Experimental Setup, then organize results by concrete RQs or evaluation questions.

## Required Opening: Experimental Setup

The setup should define:

1. Dataset, subjects, cases, participants, projects, tasks, or artifacts.
2. Baselines and why they are fair.
3. Metrics and what higher/lower values mean.
4. Experimental protocol, environment, tool versions, model versions, or hardware when relevant.
5. Statistical tests, effect sizes, qualitative coding, manual verification, or confidence intervals when relevant.
6. Reproducibility package or artifact availability.

## RQ-Based Structure

After setup, write one subsection per RQ or evaluation question:

1. State the RQ.
2. Give the short answer first.
3. Present evidence using tables, figures, numbers, examples, or qualitative categories.
4. Interpret what the evidence means for the paper's claim.
5. State boundaries or failure cases when needed.

## Tool Paper Evaluation

Typical evaluation questions:

1. Effectiveness: does the tool solve the target task better than baselines?
2. Component contribution: which module/design choice matters?
3. Scalability and robustness: does it work on larger, noisier, harder, or cross-context data?
4. Practical value: does it reduce effort, find real bugs, support real investigations, or help users?
5. Failure cases: when does the tool fail and why?

## Empirical Study Results

Typical result sections:

1. Dataset or taxonomy summary.
2. RQ1 finding with evidence.
3. RQ2 finding with evidence.
4. RQ3 finding with evidence.
5. Implications derived from the findings.
6. Sensitivity, validation, or robustness checks when needed.

## Result Paragraph Pattern

`RQ[x]: [short answer]. Table/Figure [n] shows [main evidence]. Specifically, [concrete number/result]. This indicates [interpretation], while [boundary/failure case] suggests [scope limitation].`

## Table and Figure Rules

1. One table or figure should communicate one message.
2. Label metric direction and units.
3. Keep numeric precision consistent.
4. Put statistical significance and effect size near the relevant metric.
5. Use captions to state setting, subjects, and notation.
6. Avoid hiding negative or insignificant results.

## Checklist

1. Does Evaluation start with Experimental Setup?
2. Is each result subsection tied to one RQ/evaluation question?
3. Are baselines strong, recent, and fair?
4. Are metrics valid for the SE construct?
5. Are all Introduction/Abstract claims supported by numbers, qualitative evidence, or case studies?
6. Are failure cases and negative results handled honestly?