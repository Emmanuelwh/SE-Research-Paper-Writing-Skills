# Motivating Example, Running Example, and Preliminary Study Guide

## Goal

Use this section to make the paper's problem concrete before Methodology. In SE papers, this section is not only an "example"; it can be a running object, a failure case, a preliminary study, or a compact taxonomy motivation. Its job is to help reviewers understand why the problem matters, why existing practice is insufficient, and why the later methodology or study design is necessary.

The section should answer three questions:

1. What concrete artifact, workflow, system, behavior, or empirical phenomenon should the reviewer keep in mind?
2. What does current practice miss, misinterpret, over-approximate, or handle expensively?
3. What challenge, requirement, RQ, or method component does this observation motivate?

## When to Use This Section

Add this section when the Introduction's problem statement would remain too abstract without a concrete case. It is especially useful for security, program analysis, testing, debugging, mining software repositories, empirical SE, and LLM4SE papers where the core difficulty depends on hidden context, multi-step behavior, ambiguous evidence, or human/tool interpretation.

Skip or keep it very short when the Background and Introduction already contain enough concrete examples, or when the venue/page limit makes the example less valuable than more precise methodology or evaluation detail.

## Choose the Right Form

### Motivating Example

Use this form when one concrete case can expose the central technical difficulty.

Typical flow:

1. Introduce `[artifact/workflow/case]` and the goal of the user, developer, analyst, tool, or attacker.
2. Show the surface evidence that current tools or humans can observe.
3. Explain why this evidence is insufficient or misleading.
4. Reveal the hidden semantics, missing relation, long-range dependency, behavioral condition, or contextual factor.
5. Derive the capabilities that the proposed approach must provide.

### Running Example

Use this form when the same object will be revisited throughout Methodology.

Keep the example compact and stable:

1. Define the running object and its important components.
2. Label the pieces that later method subsections will use.
3. Avoid solving the entire example in advance.
4. Refer back to the same labels in Methodology to reduce reviewer effort.

### Preliminary Study

Use this form when early empirical evidence motivates RQs, taxonomy design, dataset construction, or evaluation criteria.

Typical flow:

1. State the purpose: `To understand whether [phenomenon/problem] is systematic, we conducted a preliminary study on [sample].`
2. Describe the sampled projects, cases, commits, issues, contracts, logs, participants, or reports.
3. Summarize the analysis protocol at a high level.
4. Report motivation-level observations, not full evaluation results.
5. Derive RQs, taxonomy dimensions, design requirements, or evaluation targets.

### Motivating Failure Case

Use this form when the paper is driven by a concrete failure of existing tools, benchmarks, datasets, or practices.

Typical flow:

1. Select a small but realistic failure.
2. Explain what an existing approach sees and how it reasons.
3. Identify the wrong output, missed warning, noisy trace, incomplete diagnosis, or biased measurement.
4. Explain the consequence for developers, users, auditors, researchers, or maintainers.
5. Translate the failure into challenges that the paper addresses.

### Mini Taxonomy Motivation

Use this form when the paper needs to justify new categories or finer-grained labels.

Typical flow:

1. Present two or three cases that look similar under existing categories.
2. Show the important distinction that existing taxonomies hide.
3. Explain how the distinction affects detection, measurement, mitigation, or interpretation.
4. Use the distinction to motivate the taxonomy, RQs, or benchmark design.

## Tool Paper Patterns

Use these patterns as general scaffolding, not as fixed example types. A Tool Paper motivating example should show a concrete situation, what can be observed, why current practice is insufficient, what consequence follows, and what design requirement this creates. Do not force the example into hidden semantics, multi-view evidence, abnormal behavior, or tool-failure framing unless the paper naturally depends on that mechanism.

### General Tool-Paper Scaffold

Use for most detector, analyzer, repair, testing, auditing, debugging, reliability, security, LLM4SE, deployment, and operational papers.

Pattern bank:

- Case setup: `Consider [artifact/workflow/system/task] where [actor/tool/system] needs to [goal].`
- Observable evidence: `The available evidence is [code/log/trace/report/input/output/behavior/metadata], which suggests [initial interpretation].`
- Current limitation: `Current [tools/practices/baselines/manual processes] struggle because [missing capability/assumption/condition/cost/source of uncertainty].`
- Consequence: `As a result, [developer/user/auditor/researcher/maintainer/system] may [incorrect decision/missed issue/noisy result/high cost/delayed action].`
- Requirement bridge: `This motivates a technique that can [capability] while accounting for [constraint/scope/evidence boundary].`

### Current Practice Limitation

Use when the example mainly needs to explain why existing approaches are insufficient.

Pattern bank:

- Baseline: `A common approach is to [current practice] based on [available evidence].`
- Strength: `This works when [condition where the assumption holds].`
- Limitation: `It becomes unreliable, incomplete, or expensive when [condition where the assumption breaks].`
- Missing capability: `The missing capability is [what the approach cannot observe, connect, measure, rank, validate, or explain].`
- Paper bridge: `The proposed approach addresses this gap by [high-level method idea], which is detailed in Section X.`

### Design Requirement Derivation

Use when the example should prepare readers for method components.

Pattern bank:

- Observation: `The example exposes [observation].`
- Why it matters: `This matters because [impact on correctness, cost, reliability, generality, actionability, or trust].`
- Requirement: `Therefore, the method should [requirement].`
- Component link: `This requirement corresponds to [method component/study phase/evaluation question].`
- Boundary: `The example does not imply [overbroad claim]; it only motivates the need to handle [specific scope].`

### Example Scope Choices

Choose the smallest concrete case that exposes the paper's core difficulty.

Useful options:

1. A single artifact, input, trace, report, issue, commit, contract, test, prompt, configuration, or deployment event.
2. A short workflow with two or three steps.
3. Two contrasting cases that differ in the key factor the paper studies.
4. A compact table that maps observable evidence to limitation and design requirement.
5. A figure that labels the parts reused later in Methodology or Evaluation.

### Optional Lenses

Use these only when they fit the paper; they are not required categories.

- Normal-vs-abnormal behavior: useful when the problem is best explained by contrasting expected and problematic workflows.
- Tool or baseline failure: useful when a concrete incorrect output motivates the proposed capability.
- Semantic or contextual ambiguity: useful when the method must recover meaning, intent, state, dependency, or context from indirect evidence.
- Multiple evidence sources: useful when no single artifact, signal, or view is enough.
- Minimal artifact example: useful when a small program, input, test, log, configuration, prompt, or trace can expose the key difficulty.
## Empirical Study Patterns

### Preliminary Observation

Use when motivating that a phenomenon is common, severe, diverse, or poorly understood.

Pattern bank:

- Purpose: `To assess whether [phenomenon] is isolated or systematic, we sampled [data source].`
- Observation: `We observed that [pattern] appears across [scope], suggesting [importance].`
- Caution: `These observations are not intended as final results; they motivate a larger study of [RQ focus].`
- Bridge: `Accordingly, we ask RQ1 about [what], RQ2 about [why/how], and RQ3 about [impact/mitigation].`

### Taxonomy Motivation

Use when the study proposes or revises a taxonomy.

Pattern bank:

- Coarse category: `Existing work often groups these cases as [category].`
- Distinction: `However, the sampled cases differ in [mechanism/trigger/impact/actor/evidence].`
- Consequence: `Without separating these dimensions, evaluations may [hide failures/bias conclusions/miss emerging cases].`
- Bridge: `This motivates a taxonomy organized around [dimension 1], [dimension 2], and [dimension 3].`

### Dataset or Tool Coverage Gap

Use when motivating benchmark construction, dataset expansion, or tool comparison.

Pattern bank:

- Existing resource: `Existing datasets/tools cover [scope].`
- Missing coverage: `They provide limited support for [case type/scenario/version/ecosystem].`
- Evaluation risk: `As a result, a tool may appear effective while failing on [important cases].`
- Bridge: `This motivates our dataset construction and evaluation protocol in Section X.`

### RQ Motivation

Use when each RQ should be grounded in a concrete observation.

Pattern bank:

- RQ1: `The first observation motivates RQ1: [descriptive question].`
- RQ2: `The second observation suggests that [factor] may influence [outcome], motivating RQ2.`
- RQ3: `The final observation concerns [impact/practice/actionability], motivating RQ3.`

## Challenge Mapping

End the section by mapping concrete observations to the paper's challenges, RQs, or design requirements. This mapping should align with the Introduction and Methodology.

Recommended formats:

- Short paragraph: `The example reveals three challenges. First, [C1]. Second, [C2]. Third, [C3].`
- Table: columns for `Observation`, `Why Existing Practice Fails`, `Challenge/RQ`, and `Method or Study Response`.
- Figure caption: describe the concrete trace and point to the later method components.

Keep the mapping precise. If the Methodology has three major components, the motivating section should prepare the reviewer to understand why those components exist.

## Evidence and Numbers

Use numbers carefully. This section can include small-scale counts, illustrative measurements, or preliminary observations, but it should not become the Evaluation section.

Good uses:

1. Show that the phenomenon is not anecdotal: `[x] of [sample] cases exhibit [pattern].`
2. Show practical cost: `Manual inspection required [time/steps/tools] in this case.`
3. Show severity: `The failure affected [users/projects/assets/issues] in [scope].`
4. Show diversity: `The sampled cases cover [types/ecosystems/versions/tasks].`

Avoid:

1. Reporting all final performance metrics.
2. Overclaiming from a tiny preliminary sample.
3. Introducing numbers that are not used to motivate a specific RQ, challenge, or method component.

## Figure and Table Guidance

Use a figure or table when the example involves a trace, workflow, architecture, taxonomy, or multi-step failure.

Useful figure types:

1. Timeline or trace: show event order, state changes, or transactions.
2. Program snippet plus explanation: show the minimal code or configuration needed to expose the issue.
3. Workflow diagram: contrast benign and problematic paths.
4. Evidence table: compare what each signal/view/tool can and cannot reveal.
5. Taxonomy seed table: show why coarse labels need refinement.

Figure captions should do argumentative work: state what the reviewer should learn, not only what the figure contains.

## Writing Rules

1. Keep the example small enough for reviewers to follow in one pass.
2. Prefer concrete artifacts and observable evidence over generic claims.
3. Make the failure explicit: `[what is observed] -> [why it is misinterpreted] -> [consequence]`.
4. Use placeholders only to preserve flexibility, not to hide the logic.
5. Do not duplicate Background definitions; introduce only the concepts needed to understand the example.
6. Do not reveal the full solution before Methodology; motivate the needed capability.
7. End with a bridge to challenges, RQs, method components, or evaluation design.
8. Anonymize sensitive cases, proprietary artifacts, users, projects, addresses, organizations, or vulnerabilities when needed.

## Anti-Patterns

1. A generic story that could fit any SE paper.
2. A long background tutorial disguised as an example.
3. A final evaluation preview with too many results.
4. A single anecdote that is used to justify broad claims without caution.
5. A failure case that does not connect to any later method component or RQ.
6. A running example whose labels are never reused later.
7. A preliminary study that reports methods and results in more detail than the main study.

## Checklist

1. Does the section choose the right form: motivating example, running example, preliminary study, failure case, or taxonomy motivation?
2. Does it make the paper's problem concrete before Methodology?
3. Does it show why current solutions, datasets, tools, or practices are insufficient?
4. Does each observation map to a challenge, RQ, requirement, or method component?
5. Does it avoid duplicating Background, Methodology, and Evaluation?
6. Are examples and data anonymized or ethically safe when needed?