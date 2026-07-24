# Introduction Writing Guide

## Goal

Write an Introduction that convinces SE reviewers that the task background is important, the problem is severe, prior work is insufficient, the technical challenges are real, the methodology directly addresses those challenges, and the evaluation provides concrete evidence with numbers.

## Introduction Logic Map

Use the following logic as the default Introduction story:

1. SE context: introduce the task background, domain knowledge, motivating cases, and appropriate data.
2. Problem: explain what is difficult, costly, error-prone, understudied, or unsupported, and why the problem is harmful and urgent.
3. Prior work/current practice: summarize existing solutions or practices, then explain their limitations, impact, and consequences.
4. Gaps and challenges: state the key challenges that must be solved. These challenges should correspond to the methodology design later.
5. Methodology: use `To address these challenges, we propose [tool/method/framework], which ...`; briefly introduce the function and complete workflow, with each design choice tied to a challenge.
6. Evaluation: use `To evaluate the effectiveness of [tool/method/framework], ...`; introduce the dataset and report main experimental results with concrete numbers.
7. Contributions: summarize the empirical study, proposed method/framework, core innovation, and evaluation evidence.

## Section Skeleton

### Paragraph 1: SE Context

Introduce the task background and necessary domain knowledge.

1. Name the SE task, workflow, or ecosystem where the problem appears.
2. Explain why this task matters to developers, testers, maintainers, security analysts, researchers, organizations, or users.
3. Provide moderate motivating evidence when available: real incidents, financial loss, number of affected projects, prevalence statistics, developer effort, benchmark scale, or representative cases.
4. Keep examples and numbers focused; they should motivate the problem, not become the main result.

Useful sentence roles:

1. `[SE task/workflow] is a critical component of [software ecosystem/engineering process].`
2. `In practice, [stakeholder] must [task] when [condition].`
3. `Recent cases/statistics show that [problem] can lead to [impact].`

### Paragraph 2: Problem Severity

Explain what is difficult, costly, error-prone, understudied, or unsupported.

1. State the concrete problem after readers understand the background.
2. Explain why the problem is harmful or severe.
3. Explain why it is urgent to solve: increasing scale, high cost, security risk, developer burden, user impact, ecosystem damage, or lack of reliable support.
4. Avoid vague claims such as `important`, `challenging`, or `critical` without showing the mechanism of harm.

Useful sentence roles:

1. `However, [task] remains difficult because [reason].`
2. `This difficulty can cause [harm], especially when [condition].`
3. `Therefore, [stakeholder] urgently needs [capability/knowledge/tool support].`

### Paragraph 3: Prior Work and Current Practice

Summarize what exists and why it is insufficient.

1. Group prior methods or current practices by strategy rather than listing papers one by one.
2. For each strategy, state what it can do.
3. Then explain the limitation: what assumption it makes, what information it ignores, what scenario it cannot handle, or what cost/noise/error it introduces.
4. Explicitly state the impact and consequence of the limitation.

Useful sentence roles:

1. `Existing approaches mainly follow [strategy A] or [strategy B].`
2. `[Strategy A] can [strength], but it fails to [limitation], leading to [consequence].`
3. `[Strategy B] attempts to [strength], but it relies on [assumption], which makes it unsuitable for [target setting].`
4. `As a result, current solutions cannot reliably [desired capability].`

### Paragraph 4: Gaps and Challenges

State the gap and decompose it into challenges.

1. The gap should follow naturally from prior-work limitations.
2. List two to four concrete challenges that must be solved.
3. Each challenge should explain why the problem is hard, not merely restate a missing feature.
4. Each challenge should map to a later methodology component.
5. Use challenge labels if they improve clarity: `C1`, `C2`, `C3`.

Challenge-to-method mapping rule:

1. If the Introduction states `C1`, the Methodology paragraph should include a design that addresses `C1`.
2. If the Methodology introduces a major component, the Introduction should have already motivated why it is needed.
3. Do not introduce a challenge that the method does not solve or evaluate.

Useful sentence roles:

1. `Addressing this gap requires overcoming three challenges.`
2. `First, [C1] is difficult because [reason].`
3. `Second, [C2] requires [capability], but [obstacle].`
4. `Third, [C3] becomes challenging when [hard setting].`

### Paragraph 5: Methodology

Introduce the proposed method, framework, or tool and connect the design to the challenges.

1. Start with `To address these challenges, we propose [name], a [tool/method/framework] that [main function].`
2. Briefly introduce what the tool/method does and what problem it solves.
3. Present the complete workflow in execution order.
4. Explain each step's purpose, input, output, and connection to the next step.
5. Make the design explicitly respond to the challenges from the previous paragraph.
6. Keep details concise; save algorithms, implementation, and formal definitions for Methodology.

Useful sentence roles:

1. `To address these challenges, we propose [name], which [core capability].`
2. `Given [input], [name] first [step 1], producing [output 1] to address [C1].`
3. `It then [step 2], which [purpose] and addresses [C2].`
4. `Finally, [name] [step 3], generating [final output] for [downstream use].`

### Paragraph 6: Evaluation

Preview evaluation with concrete datasets, experiments, and numerical results.

1. Start with `To evaluate the effectiveness of [name], we ...`.
2. Introduce the dataset: size, source, task, time span, project/language coverage, subjects, cases, or real-world artifacts.
3. Summarize main experiments: comparison with baselines, ablation, robustness, scalability, real-world deployment, case study, bug finding, bug bounty, user study, or qualitative analysis.
4. Use concrete numbers and results when available.
5. Ensure every number is traceable to the Evaluation section.
6. Avoid reporting unsupported numbers in the Introduction.

Useful sentence roles:

1. `To evaluate the effectiveness of [name], we evaluate it on [dataset], containing [scale/scope].`
2. `Experimental results show that [name] achieves [metric/result], outperforming [baseline] by [number] or improving [metric] by [number].`
3. `Ablation/case-study/real-world results further show that [component/effect].`
4. `These results demonstrate [bounded claim].`

### Paragraph 7: Contributions

End with a concise contribution list after the story has made the contributions necessary.

1. Include an empirical-study contribution when the paper contains an empirical study, controlled experiment, interview, survey, or mixed-methods study.
2. Include the proposed method/framework/tool and the problem it solves.
3. Include the core design or innovation and the challenge it addresses.
4. Include evaluation evidence with concrete experimental results.

## Contribution Framing

Use contribution bullets that are specific, evidence-aware, and aligned with the Introduction story.

### 0) Empirical Study Contribution

Use when the paper includes empirical studies, controlled experiments, interviews, surveys, or mixed-methods studies.

`We conduct [an empirical study/a controlled experiment/interviews/a survey/a mixed-methods study] on [dataset/participants/artifacts] to understand [phenomenon/problem], revealing [main finding/insight].`

### 1) Method or Framework Contribution

Use for the main tool, method, framework, system, detector, analyzer, benchmark pipeline, or technique.

`We propose/develop [method/framework/tool] for [target task], addressing [specific problem] in [SE setting].`

Better version:

`We propose [name], a [method/framework/tool] that [main capability], enabling [stakeholder] to [desired outcome] under [target setting].`

### 2) Core Innovation Contribution

Use to highlight the key design that solves the central challenge.

`To address [challenge], we design [core component/representation/algorithm/workflow], which [technical idea] and enables [benefit].`

When there are multiple challenges, use one bullet that names the integrated design rather than a long component list.

### 3) Evaluation Contribution

Use to summarize experimental evidence with concrete results.

`We evaluate [name] on [dataset/subjects/tasks]. Experimental results show that [main numerical result], and [case study/ablation/real-world validation] further demonstrates [practical effect].`

Do not write `Experimental results show that our method is effective` without naming the metric, dataset, comparison, or concrete result.

## Alignment Rules

1. Every challenge should map to one methodology design choice.
2. Every methodology design choice should be motivated by a prior challenge.
3. Every major claim in Methodology should be previewed or supported by Evaluation.
4. Every number in Introduction should be repeated or justified in Evaluation.
5. Every contribution bullet should correspond to a section in the paper.

## SE-Specific Checks

1. Does the first paragraph give enough background knowledge for a non-specialist SE reviewer?
2. Are motivating cases and data relevant but not excessive?
3. Does the problem paragraph explain severity and urgency?
4. Does prior work explain limitations, impacts, and consequences rather than merely saying methods are insufficient?
5. Are the challenges concrete and mapped to methodology components?
6. Does the methodology paragraph describe a complete workflow with input-output relations?
7. Does the evaluation paragraph include dataset details and concrete numerical results?
8. Are contribution bullets specific, evidence-aware, and aligned with the story?

## Common Failure Modes

1. Starting with broad software importance without explaining the specific task background.
2. Introducing many incident examples or statistics without connecting them to the research problem.
3. Saying prior work is limited without explaining the impact or consequence of the limitation.
4. Listing challenges that the proposed method does not address.
5. Describing the method as a black box without workflow, step purpose, or input-output relation.
6. Reporting evaluation claims without concrete numbers.
7. Ending with contribution bullets that are generic or disconnected from the challenges.