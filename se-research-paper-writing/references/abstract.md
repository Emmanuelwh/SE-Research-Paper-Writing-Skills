# Abstract Writing Guide

## Goal

Write an abstract that lets an SE reviewer understand the problem, gap, contribution, evidence, and implications within one pass.

## Pre-Writing Questions

Before drafting, answer:

1. What concrete SE problem does the paper address?
2. Who experiences the problem: developers, maintainers, testers, security analysts, researchers, tool builders, or organizations?
3. What is missing in prior work or current practice?
4. What does the paper contribute: empirical finding, method, tool, dataset, benchmark, taxonomy, theory, or replication?
5. What evidence supports the contribution?
6. What is the practical or research implication?

## Default Abstract Structure

1. Context: introduce the SE setting and why it matters.
2. Problem/gap: state what remains difficult or unknown.
3. Approach/study: describe the artifact, method, or empirical design.
4. Evidence: report the main dataset, benchmark, participants, projects, metrics, or results.
5. Implication: explain what the finding/tool enables for SE researchers or practitioners.

## Templates by Paper Type

### Empirical Study

1. Context: `[SE activity] depends on [phenomenon/process/artifact].`
2. Gap: `However, little is known about [specific behavior/condition/impact].`
3. Study: `We conducted [study type] on [data/participants/projects] to answer [RQs].`
4. Findings: `Our results show that ...`
5. Implication: `These findings suggest ... for [stakeholder].`

### Tool/System Paper

1. Context: `[Stakeholder] needs to [task] during [SE workflow].`
2. Gap: `Existing tools struggle with [limitation].`
3. Contribution: `We present [tool], which [core technical idea].`
4. Evaluation: `We evaluate [tool] on [subjects/tasks] against [baselines].`
5. Implication: `The results indicate that [tool] can ...`

### Program Analysis, Testing, or Verification

1. Context: `[Analysis/testing/verification task] is important for [quality/security/reliability].`
2. Gap: `Prior techniques are limited by [precision/recall/scalability/soundness/usability constraint].`
3. Technique: `We propose [technique], which [key design].`
4. Evaluation: `On [benchmarks/projects], [technique] achieves ...`
5. Boundary: `The results highlight both [strength] and [limitation].`

### LLM4SE or AI4SE

1. Context: `Large language models are increasingly used for [SE task].`
2. Gap: `Yet their behavior under [realistic SE condition] remains unclear/limited.`
3. Study/Method: `We evaluate/propose [approach] using [tasks/data/models/prompts].`
4. Evidence: `Results show ...`
5. Implication: `These findings provide guidance for [using/designing/evaluating] LLM-based SE tools.`

## Quality Checklist

1. Does the first sentence identify a real SE setting, not a generic AI/software claim?
2. Does the abstract state a gap, not just a task?
3. Are study scale and evidence concrete enough?
4. Are all numeric claims traceable to Evaluation?
5. Are causal/general claims supported by the design?
6. Is the final implication useful but not overclaimed?
