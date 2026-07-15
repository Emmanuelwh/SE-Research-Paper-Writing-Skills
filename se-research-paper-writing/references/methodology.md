# Methodology Writing Guide

## Goal

Write Methodology so reviewers can judge whether the study or technique is sound, reproducible, and aligned with the research questions.

## Pre-Writing Questions

1. What are the research questions or evaluation goals?
2. What paper type is this: empirical study, tool/system, program analysis/testing, MSR, LLM4SE, or security-for-SE?
3. What are the subjects: projects, commits, issues, bugs, vulnerabilities, tests, participants, tasks, or benchmarks?
4. How were subjects selected, filtered, and cleaned?
5. What variables, labels, metrics, or constructs are operationalized?
6. What procedure was followed step by step?
7. What baselines, comparison groups, or controls are used?
8. What analysis method is used: statistical test, effect size, qualitative coding, thematic analysis, manual inspection, or case study?
9. What artifacts are available for replication?

## Core Structure

1. RQs or study goals.
2. Subject/data selection.
3. Data collection and preprocessing.
4. Method/tool/system design or study procedure.
5. Measures, metrics, labels, and operational definitions.
6. Analysis method.
7. Implementation and reproducibility details.

## Paper-Type Guidance

### Empirical Study

Include sampling strategy, inclusion/exclusion criteria, data cleaning, coding protocol, inter-rater agreement when applicable, statistical tests, effect sizes, and ethics/consent when human subjects are involved.

### Tool/System Paper

Include design goals, architecture, workflow integration, implementation details, required inputs/outputs, failure behavior, and reproducibility package. Make clear what is an engineering design decision and what is a research contribution.

### Program Analysis, Testing, or Verification

Include problem formulation, assumptions, algorithm steps, soundness/precision tradeoffs, implementation choices, benchmark construction, oracle definition, and scalability considerations.

### MSR Paper

Include repository selection, data extraction APIs, time window, deduplication, bot filtering, label construction, missing-data handling, and bias introduced by platform behavior.

### LLM4SE Paper

Include model versions, prompts, decoding parameters, context construction, data leakage controls, benchmark contamination concerns, human evaluation protocol, and cost/reliability considerations.

## Writing Rules

1. Present Methodology before results; do not smuggle results into procedure descriptions.
2. Define constructs before measuring them.
3. Make every metric interpretable: what does a higher value mean and why does it answer the RQ?
4. State exclusions transparently and justify them.
5. Use tables for datasets, subject systems, RQs, metrics, and baselines when they reduce ambiguity.

## Methodology Checklist

1. Can a reviewer reproduce the study design from this section?
2. Does each RQ have a corresponding method and analysis?
3. Are subject selection and filtering criteria explicit?
4. Are metrics and labels valid proxies for the intended constructs?
5. Are baselines fair and relevant?
6. Are ethical and reproducibility details included when needed?
