# Abstract Writing Guide

## Goal

Write an abstract that lets an SE reviewer understand the background, gap, contribution, evidence, and implication within one pass. The abstract should not over-separate paper types too early; first follow the shared structure, then adapt it to either a Tool Paper or an Empirical Study.

## Pre-Writing Questions

Before drafting, answer:

1. What concrete software engineering problem does the paper address?
2. Why is this problem important or severe for developers, maintainers, testers, security analysts, researchers, tool builders, or organizations?
3. What is missing or insufficient in existing tools, solutions, or studies?
4. What is the paper's main contribution: a tool/technique or an empirical study?
5. What evidence supports the contribution?
6. What implication should SE researchers or practitioners take away?

## Overall Abstract Structure

Use this shared structure before choosing a paper-type template:

1. Context: introduce the problem background and the SE setting.
2. Gap: explain what existing tools, solutions, or studies fail to address, and what consequence this causes.
3. Contribution: state what the paper proposes or studies.
4. Evidence: summarize the dataset, evaluation/study design, main experiments, findings, or real-world evidence.
5. Implication: explain what the contribution means for SE researchers, practitioners, tools, or future work.

## Templates by Paper Type

Only distinguish two high-level types: Tool Paper and Empirical Study.

### Tool Paper

Use this template when the main contribution is a tool, system, technique, framework, detector, analyzer, repair method, benchmarked pipeline, or practical workflow support.

1. Context: introduce the problem background.
   - State the SE task or workflow where the problem appears.
   - Identify who is affected and why the problem matters.
   - Example role: `Developers/security analysts/testers need to [task] during [workflow].`
2. Gap: explain the problems in existing tools or solutions and the consequences.
   - State what current tools cannot handle, assume, miss, or make costly.
   - Explain the concrete consequence, such as missed bugs, inaccurate triage, high manual effort, poor scalability, weak reproducibility, or limited deployment value.
   - Example role: `However, existing tools struggle with [limitation], which leads to [consequence].`
3. Technique: state `We propose [name], which ...`, then briefly explain the complete workflow.
   - Start with the main technical idea.
   - Describe the workflow in execution order.
   - Make each step's purpose clear.
   - Make the input-output relationship clear: what each step takes as input, what it produces, and how that output feeds the next step.
   - Keep this concise; the abstract should show the whole pipeline, not method details.
   - Example role: `We propose [tool/technique], which [core idea]. Given [input], it first [step 1/purpose/output], then [step 2/purpose/output], and finally [step 3/purpose/output].`
4. Evaluation: introduce the dataset and evidence.
   - Use `We evaluate [tool/technique] on [dataset/subjects/tasks].`
   - Mention main experiments, such as comparison with baselines, ablation, scalability, robustness, or accuracy.
   - Mention case study, real-world deployment effect, discovered bugs, bug bounty result, developer feedback, or practical evidence when available.
   - Example role: `We evaluate [tool] on [dataset], comparing it with [baselines] and conducting [case study/real-world validation/bug bounty validation].`
5. Implication: state the practical or research value.
   - Explain what the tool enables, improves, reveals, or makes practical.
   - Scope the implication to the evaluated setting.

### Empirical Study

Use this template when the main contribution is understanding, measuring, characterizing, explaining, or deriving implications from software engineering data or human/software artifacts.

1. Context: introduce the problem background and severity.
   - State the SE phenomenon or workflow being studied.
   - Explain why the issue is important, frequent, costly, risky, or underexplored.
   - Example role: `[SE phenomenon] affects [stakeholder/workflow], making it important to understand [issue].`
2. Gap: explain what existing research has not studied and the consequence.
   - State what remains unknown, under-measured, or insufficiently explained.
   - Explain why this missing knowledge matters for researchers, practitioners, tools, or policy.
   - Example role: `However, existing studies have not [missing knowledge], leaving [stakeholder] without [consequence].`
3. Study: introduce the dataset in detail and state the study design.
   - Use `We conducted [study type] on [dataset/subjects/artifacts].`
   - Summarize the dataset scale, source, time span, project/language/domain coverage, participants, labels, or artifacts when relevant.
   - Make clear what is observed or measured.
   - Example role: `We conducted [empirical study] on [N projects/N issues/N commits/N participants], covering [scope], to answer [RQs].`
4. Findings: briefly introduce each RQ and its result.
   - Follow the defined RQs instead of listing disconnected findings.
   - For each RQ, state the question focus and the main answer.
   - Keep results concrete but concise; include key numbers only when they are central and traceable to Evaluation.
   - Example role: `For RQ1, we find that ...; for RQ2, ...; for RQ3, ...`
5. Implication: explain what the findings mean.
   - State implications for SE researchers, practitioners, tool builders, dataset designers, benchmark users, or future empirical studies.
   - Avoid overclaiming causality or generality beyond the studied data.

## Quality Checklist

1. Does the first sentence identify a concrete SE setting rather than a generic software or AI claim?
2. Does the abstract state both the gap and the consequence of that gap?
3. For Tool Papers, does the technique sentence explain the workflow, step purposes, and input-output chain clearly enough?
4. For Tool Papers, does the evaluation mention dataset, main experiments, and practical evidence such as case study, real-world effect, or bug bounty when available?
5. For Empirical Studies, does the abstract introduce the dataset scale and study design concretely?
6. For Empirical Studies, are findings organized by RQ rather than as disconnected claims?
7. Are all numeric or comparative claims traceable to the Evaluation section?
8. Are causal, generality, and practical-impact claims scoped to the evidence?
9. Does the final implication tell reviewers why the work matters for SE research or practice?