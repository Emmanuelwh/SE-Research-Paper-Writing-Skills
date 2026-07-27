# Evaluation Writing Guide

## Goal

Write Evaluation so reviewers can see whether the tool actually supports the paper's central SE task. For Tool Papers, Evaluation should be organized around research questions, begin with a complete experimental setup, and then answer each RQ with tables, figures, case evidence, and careful interpretation.

The Evaluation section should test the claims made in Abstract, Introduction, and Methodology. It should not merely report numbers. It should explain what each result means, why the result occurs, and what boundary remains.

## RQ Design for Tool Papers

Start Evaluation by stating the research questions before Experimental Setup.

Opening pattern:

`We aim to address the following research questions:`

Design RQs by mapping each major paper claim to one evaluation question. A typical Tool Paper does not need every possible RQ below, but it should usually cover effectiveness, comparison with strong methods or current practice, module contribution, and real-world usefulness when those claims appear in the paper.

### Core RQ Types

1. Effectiveness: test whether the tool solves the main task.
   - Example: `RQ1: How effective is [Tool] in [detecting/repairing/classifying/generating/analyzing] [target cases]?`
   - Use this RQ for the primary claim of the paper.
   - Report task-appropriate metrics and compare against meaningful alternatives when possible.

2. Baseline or SOTA comparison: test whether the tool improves over existing methods or current practice.
   - This can be a separate RQ or part of the effectiveness RQ.
   - Keep it inside effectiveness when the main table already compares all methods on the same benchmark.
   - Make it a separate RQ when the paper needs deeper analysis of why existing methods fail or where they remain strong.
   - Example: `RQ2: How does [Tool] compare with existing [tools/methods/practices] under the same evaluation protocol?`

3. Ablation study: test whether the proposed modules or design choices are necessary.
   - Example: `RQ3: How much does each major component of [Tool] contribute to the final result?`
   - Ablate modules from Methodology, not arbitrary implementation details.
   - Use remove, replace, weaken, or disable variants and report the change relative to the full tool.

4. Real-world evaluation: test whether the tool works beyond a controlled benchmark.
   - Example: `RQ4: Can [Tool] find real [bugs/vulnerabilities/failures/misconfigurations/maintenance issues] in real-world projects?`
   - For security and reliability papers, include manual confirmation, responsible disclosure status, developer response, patch status, or case studies when possible.
   - For broader SE tools, evaluate across projects, ecosystems, versions, tasks, or usage scenarios.

### Optional RQ Types

Use these only when the paper claims them:

1. Efficiency or scalability: `RQ: How efficiently does [Tool] run on [project scale/input size]?`
2. Robustness or sensitivity: `RQ: How sensitive is [Tool] to [threshold/model/prompt/data quality/project setting]?`
3. Usability or developer usefulness: `RQ: How do developers/users perceive or use [Tool]'s output?`
4. Failure analysis: `RQ: When does [Tool] fail, and why?`

### RQ Ordering

A common order is:

1. Main effectiveness.
2. Comparison with baselines or SOTA methods.
3. Ablation or design contribution.
4. Real-world applicability, generalization, scalability, or case study.
5. Failure analysis if substantial enough to deserve its own subsection.

If baseline comparison is included in RQ1, use this order instead:

1. Effectiveness with baselines.
2. Ablation.
3. Real-world evaluation or generalization.
4. Efficiency, robustness, usability, or failure analysis.

Example reference:

- `references/examples/evaluation/rq-design-tool-paper.md`

## Part 1: Experimental Setup

Place Experimental Setup immediately after the RQs. The setup should make the evaluation reproducible and fair before any results are shown.

### Dataset or Subjects

Explain how the dataset, benchmark, projects, cases, tasks, or real-world subjects were obtained.

Required content:

1. Data source: where the data comes from and why it matches the paper's target setting.
2. Collection process: search query, crawl method, time window, repository selection, benchmark source, incident source, or task generation process.
3. Inclusion and exclusion criteria: what is kept, what is removed, and why.
4. Ground truth or labeling: how labels are obtained, verified, or adjudicated.
5. Objectivity and coverage: how the dataset avoids cherry-picking and covers diverse projects, ecosystems, versions, case types, severities, or scenarios.
6. Dataset summary: number of projects, artifacts, cases, tasks, bugs, vulnerabilities, commits, reports, tests, participants, or samples.

Dataset paragraph pattern:

`We constructed the dataset from [source] because [reason]. We included [criteria] and excluded [criteria] to ensure [quality/objectivity]. To reduce selection bias, we [random sampling/systematic search/multiple sources/time-window coverage/domain coverage]. The final dataset contains [scale], covering [diversity dimensions]. Ground truth was obtained by [labeling/verification/source], with [agreement/adjudication/manual confirmation] when applicable.`

### Metrics

Introduce metrics after the dataset because metrics should measure the task defined by the data.

Required content:

1. Metric names and formulas when not standard.
2. What each metric measures in SE terms.
3. Whether higher or lower is better.
4. Why the metric matches the paper's claim.
5. Any human-effort, actionability, severity, or confirmation metrics when relevant.

Common metric families:

1. Classification/detection: precision, recall, F1, false positive rate, false negative rate, AUC, top-k precision.
2. Ranking/prioritization: MRR, MAP, NDCG, top-k hit rate, inspection effort saved.
3. Repair/generation: correctness rate, test pass rate, patch acceptability, compilation rate, human preference, semantic equivalence.
4. Security/reliability: confirmed bugs, confirmed vulnerabilities, severity, exploitability, disclosure status, patch status, affected projects.
5. Efficiency/scalability: runtime, memory, throughput, cost, API calls, manual effort.
6. Study/tool usability: task completion, time saved, user rating, qualitative themes.

Metric paragraph pattern:

`We use [metric] to measure [construct] because [reason]. Higher/lower values indicate [interpretation]. For [special task], we additionally report [metric] to capture [actionability/cost/severity/real-world value].`

### Baselines and Compared Methods

Introduce baselines before results so reviewers can judge fairness.

Required content:

1. What each baseline represents: SOTA, strongest public tool, current practice, heuristic, commercial tool, or prior benchmark winner.
2. Why each baseline is relevant.
3. Whether it is run with official implementation, reimplementation, API, or reported numbers.
4. How protocol fairness is maintained: same dataset, same preprocessing, same ground truth, same budget, same prompts, same hardware, or same time limit.
5. Any adaptation needed to make the baseline applicable.

Baseline paragraph pattern:

`We compare [Tool] with [baseline] because it represents [SOTA/current practice/simple heuristic]. We use [official implementation/reimplementation/API] and run all methods on the same [dataset/protocol]. When adapting [baseline] to our setting, we [adaptation] and keep [fairness constraint] unchanged.`

### Implementation and Environment

Evaluation setup should include the implementation details needed to reproduce reported results. Do not repeat all Methodology internals; report the concrete experimental configuration.

Required content:

1. Programming language, framework, libraries, solvers, model/API versions, parser versions, or toolchain versions.
2. Hardware, OS, runtime environment, and parallelism when runtime or scalability is reported.
3. Hyperparameters, thresholds, prompt settings, decoding settings, seeds, timeouts, or resource budgets used in experiments.
4. Artifact availability: code, data, scripts, Docker image, replication package, or anonymized release.

Implementation paragraph pattern:

`We implemented [Tool] in [language] using [framework/library/toolchain]. Experiments were run on [hardware/OS] with [resource setting]. Unless otherwise stated, we used [configuration]. We will release [artifact] to support replication.`

Example reference:

- `references/examples/evaluation/experimental-setup-example.md`

## Part 2: Writing Each RQ Subsection

After Experimental Setup, write one subsection per RQ. Each RQ subsection should answer the question first, then present evidence, then analyze why the result occurs.

### Required RQ Subsection Structure

1. RQ title and question: make the subsection title or first sentence state the RQ.
2. Short answer: give the main result in one sentence before details.
3. Result presentation: introduce the table, figure, chart, or case study and explain what it shows.
4. Detailed result: report the key numbers, comparisons, trends, or qualitative observations.
5. Analysis: explain why the result occurs, connecting back to Methodology modules, dataset properties, or baseline limitations.
6. Boundary or failure case: state where the result is weaker, unsupported, or limited.
7. Takeaway: end with a concise answer to the RQ.

RQ paragraph pattern:

`RQ[x]: [short answer]. Table/Figure [n] shows [main evidence]. Specifically, [concrete result]. This result suggests [interpretation]. The improvement/limitation occurs because [reason tied to module, dataset, or baseline behavior]. However, [boundary/failure case]. Therefore, [bounded answer to RQ].`

### Result Presentation

Before analyzing, orient the reader to the table or figure.

Good presentation patterns:

1. `Table X reports [metrics] for [methods] on [datasets/settings].`
2. `Figure X shows how [metric] changes as [input size/project size/noise level/threshold] increases.`
3. `Table X compares the full tool with variants that remove [module/design choice].`
4. `Figure X summarizes the real-world findings by [severity/project/ecosystem/status].`
5. `Table X reports confirmed bugs and developer responses for [real-world setting].`

### Analysis of Causes

Do not stop after reporting that one method is better. Explain why.

Useful analysis sources:

1. Methodology: which module or design choice creates the gain?
2. Baseline behavior: what assumption causes the baseline to miss, over-report, or mis-rank cases?
3. Dataset properties: which case types, project scales, languages, or scenarios affect performance?
4. Error analysis: what failure cases reveal the method's boundary?
5. Real-world validation: which findings were confirmed, patched, reproduced, or rejected?

Analysis pattern:

`The gain mainly comes from [module/design choice], which [mechanism]. In contrast, [baseline] relies on [assumption], causing [failure mode] when [condition]. The remaining errors occur when [condition], suggesting that [boundary].`

Example reference:

- `references/examples/evaluation/rq-result-analysis-example.md`

## Table and Figure Rules

1. One table or figure should communicate one message.
2. Label metric direction and units, such as `Precision ¡ü`, `Runtime (s) ¡ý`, or `Confirmed Bugs ¡ü`.
3. Keep numeric precision consistent.
4. Put statistical significance, confidence intervals, or effect sizes near the relevant metric when used.
5. Use captions to state setting, subjects, metrics, and notation.
6. Avoid hiding negative, insignificant, or failure results.
7. For ablation tables, include the full tool and variants with one clear design removed, replaced, or weakened.
8. For real-world evaluation, include confirmation status and examples when possible, not only counts.

## Common RQ-Specific Guidance

### Effectiveness

1. Use the primary dataset and primary metrics.
2. Compare with strong baselines when available.
3. Report both absolute performance and relative improvement.
4. Explain which case types are easier or harder.

### SOTA or Existing Methods

1. State why each compared method is a fair and strong reference point.
2. Explain where existing methods still perform well.
3. Analyze failure reasons rather than only claiming superiority.
4. Avoid comparing against weak baselines only.

### Ablation Study

1. Tie each ablation to a Methodology module or design claim.
2. Use variants that are interpretable: remove, replace, weaken, or disable one design choice.
3. Report delta from the full tool.
4. Explain what the delta means about the module's necessity.
5. If modules interact, include combined ablations or explain why isolated ablation is misleading.

### Real-World Evaluation

1. Explain how real-world subjects are selected.
2. Report confirmation protocol: manual analysis, reproduction, developer response, disclosure, patch, or external validation.
3. For security papers, distinguish confirmed vulnerabilities, suspected issues, false positives, duplicates, and out-of-scope cases.
4. Include representative cases that show practical value and boundaries.
5. Avoid claiming real-world impact from unverified alerts alone.

## Checklist

1. Does Evaluation start by listing clear RQs?
2. Does each RQ map to a claim from Abstract, Introduction, or Methodology?
3. Does Experimental Setup explain Dataset, Metrics, Baselines, Implementation, and Environment?
4. Are dataset collection criteria objective and comprehensive enough for the claim?
5. Are metrics appropriate for the SE construct being measured?
6. Are SOTA or current-practice baselines fair and clearly configured?
7. Does each RQ subsection answer first, then present evidence, then analyze causes?
8. Are ablations tied to actual modules or design choices?
9. Does real-world evaluation include confirmation or case evidence when needed?
10. Are weak results, failure cases, and scope boundaries discussed honestly?