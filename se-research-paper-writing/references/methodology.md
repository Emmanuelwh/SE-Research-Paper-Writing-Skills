# Methodology Writing Guide

## Goal

Write Methodology so reviewers can understand the full design before reading details. Always start with an overall overview, then write concrete subsections for modules, study phases, algorithms, data processing steps, or analysis components.

## Required Opening: Overall Overview

The first Methodology subsection should answer:

1. What is the input?
2. What is the output?
3. What are the main stages/components?
4. Which challenge or RQ does each stage address?
5. How does information flow from one stage to the next?

Use a figure or pipeline table when the method has multiple modules.

## Tool Paper Structure

1. Overview: full workflow, inputs, outputs, and challenge mapping.
2. Problem formulation or design goals.
3. Component 1: motivation, input, operation, output, and addressed challenge.
4. Component 2: motivation, input, operation, output, and addressed challenge.
5. Component 3 or integration/fusion/decision module.
6. Implementation details and reproducibility notes.

## Empirical Study Structure

1. Study overview: RQs, data sources, and analysis pipeline.
2. Data collection: sources, time window, sampling, inclusion/exclusion criteria.
3. Data preprocessing: cleaning, filtering, deduplication, normalization, labeling.
4. Measurement or operationalization: variables, constructs, metrics, coding scheme.
5. Analysis method: statistical analysis, qualitative coding, manual inspection, case study, or mixed methods.
6. Reproducibility: artifacts, scripts, annotation protocol, prompts, and replication package.

## Component Writing Pattern

For each component/subsection, write:

1. Motivation: why this component is needed.
2. Input: what data/artifact/state it receives.
3. Design: how it works.
4. Output: what it produces.
5. Link: how the output feeds the next component or answers an RQ.
6. Advantage: why this design addresses the stated challenge.

## Semi-Template

`Given [input], the overview pipeline first [stage 1] to produce [output 1], then [stage 2] to address [challenge/RQ], and finally [stage 3] to generate [final output]. Section [x] describes [component 1], Section [y] describes [component 2], and Section [z] explains [integration/analysis].`

## Checklist

1. Does Methodology begin with an overview?
2. Does every challenge/RQ from Introduction map to a method or study-design element?
3. Are inputs and outputs explicit for every major step?
4. Are data collection, preprocessing, labels, metrics, and analysis methods clear when this is an Empirical Study?
5. Are implementation and reproducibility details sufficient for reviewer trust?