# Background, Research Object, Problem Statement, and Threat Model Guide

## Goal

Write this section so reviewers have enough domain knowledge to understand the paper's research object, problem definition, methodology, and evaluation. The section should be compact, functional, and strongly tied to the paper. It should explain the concepts, objects, roles, workflows, and assumptions that the later sections rely on, rather than giving a broad textbook survey.

For most SE papers, keep this part to at most 3-4 subsections:

1. Background Concepts
2. Running Object / Research Object
3. Problem Statement
4. Threat Model or Assumptions, only when needed

The subsections do not need to follow a rigid template. Use flexible sentence roles and choose only the pieces needed by the paper.

## When to Include This Section

Include this section when the paper depends on concepts that a general SE reviewer may not know well enough, such as blockchain execution, DeFi protocols, smart contract semantics, compiler internals, program analysis abstractions, testing workflows, developer processes, LLM prompting pipelines, security assumptions, or domain-specific datasets.

Use this section to define the paper's research object clearly. The research object may be a subject system, artifact type, software ecosystem, workflow, vulnerability class, fraud pattern, tool behavior, developer behavior, benchmark object, or a class of problems studied by the paper.

Include a Problem Statement when the paper needs a precise task definition, input/output, assumptions, scope, objective, or success criteria.

Include a Threat Model or Assumptions subsection when the paper involves security, abuse, adversaries, attacks, vulnerabilities, fraud, malware, privacy, misuse, or any setting where reviewer trust depends on explicit assumptions.

## Recommended Structure

Use at most 3-4 subsections. Do not split background into many small textbook sections unless the paper truly needs them.

### 1) Background Concepts

Define only the concepts needed later in the paper.

1. Introduce domain concepts that appear in Introduction, Methodology, and Evaluation.
2. Define abbreviations, entities, protocols, workflows, or technical terms before reusing them.
3. Explain how a concept works only to the level needed by the paper.
4. Use small examples when a concept is hard to understand.
5. Avoid unrelated history, broad surveys, or implementation details that do not support the paper's research object.

Flexible pattern bank. Pick and combine as needed:

- Definition: `[Concept] is/refers to [short definition].`
- Scope: `In this paper, we focus on [specific platform/system/workflow] where [concept] has [relevant property].`
- Mechanism: `[Concept] works by [high-level mechanism], enabling [operation/use].`
- Role in the paper: `This concept matters because [later method/evaluation/problem] relies on [specific property].`
- Minimal example: `For example, [small example] illustrates [one relevant behavior].`
- Contrast: `Unlike [related concept], [concept] [key difference relevant to the paper].`

Use this style for background concepts such as smart contracts, transactions, token standards, compilers, tests, traces, prompts, issue reports, or vulnerability categories.

### 2) Running Object / Research Object

Define the main subject system or the class of problems studied by the paper.

1. For Tool Papers, define the object the tool operates on: programs, contracts, transactions, issues, pull requests, tests, logs, traces, prompts, vulnerabilities, attacks, or workflows.
2. For Empirical Studies, define what is being studied: a phenomenon, behavior, vulnerability class, tool family, dataset object, developer practice, ecosystem process, or problem category.
3. Explain the object's key components, lifecycle, roles, observable evidence, and why it is the right unit of analysis.
4. If useful, introduce a running example that will be reused in Methodology or Motivating Example.
5. When the object has normal and abnormal forms, describe both; this is especially useful for security papers.

Flexible pattern bank. Pick and combine as needed:

- Object focus: `The main object studied in this paper is [object/problem class].`
- Components: `It involves [component/entity/role A], [component/entity/role B], and [component/entity/role C].`
- Lifecycle/workflow: `A typical workflow proceeds as follows: [stage 1] -> [stage 2] -> [stage 3].`
- Roles: `[Role A] performs [action], while [Role B] [action].`
- Observable evidence: `This object can be observed through [code/transaction/log/test/issue/prompt/trace/behavior].`
- Normal case: `In a benign or legitimate case, [expected workflow/behavior].`
- Abnormal case: `In contrast, [malicious/faulty/undesired case] mimics or deviates from this workflow by [key difference].`
- Relevance: `This distinction is important because [method/RQ/evaluation] depends on recognizing [property].`

For example, a security paper may first explain the normal workflow of an artifact, then contrast it with how an attack or abuse pattern follows the same early steps but diverges at a critical point.

### 3) Problem Statement

Formalize the task or study target after readers understand the background and research object.

1. Define the input.
2. Define the output, decision, trace, label, taxonomy, or expected finding.
3. Define the scope and assumptions.
4. Define success criteria, objective, or evaluation target.
5. Keep notation consistent with Methodology and Evaluation.

Flexible pattern bank. Pick and combine as needed:

- Task input: `The input is [artifact/data/context], possibly together with [auxiliary information].`
- Task output: `The expected output is [label/ranking/report/trace/topology/taxonomy/finding].`
- Objective: `The goal is to [detect/trace/classify/repair/measure/characterize/explain] [target object].`
- Scope: `We focus on [in-scope setting] and exclude [out-of-scope setting].`
- Requirement: `A useful solution should [requirement 1], [requirement 2], and [requirement 3].`
- Success criterion: `We consider the task successful when [evaluation criterion].`
- RQ bridge: `This formulation leads to [RQ/evaluation question], which asks [question].`

Do not force a mathematical formulation unless the paper benefits from one. For many SE papers, a precise prose definition plus input/output/scope is enough.

### 4) Threat Model or Assumptions

Include this subsection for security-sensitive or assumption-heavy papers.

1. Define adversary capability when the paper studies attacks, abuse, vulnerabilities, fraud, or misuse.
2. Define defender observations and goals when the paper proposes detection, tracing, repair, mitigation, or analysis.
3. Define trusted and untrusted components.
4. State what is out of scope.
5. For non-security papers, use this subsection as `Assumptions` only if the methodology depends on explicit constraints.

Flexible pattern bank. Pick and combine as needed:

- Adversary capability: `We consider an adversary who can [capability].`
- Adversary constraint: `The adversary cannot [constraint] or is assumed not to [out-of-scope action].`
- Defender observation: `The defender observes [available evidence] but does not observe [hidden information].`
- Defender goal: `The defender aims to [detect/trace/prevent/repair/measure] [target].`
- Trust boundary: `We assume [trusted component/data/source] is [assumption], while [untrusted component] may [risk].`
- Out of scope: `[case/action/setting] is outside the scope of this paper because [reason].`
- Discussion bridge: `We revisit [remaining assumption/limitation] in Discussion or Threats to Validity.`

Use this subsection to bound claims, not to overcomplicate the background.

## Background Writing Rules

1. Do not write a textbook survey.
2. Keep the section to at most 3-4 subsections whenever possible.
3. Use flexible sentence roles rather than forcing a single template.
4. Define terms before using abbreviations or custom terminology.
5. Prefer task-relevant definitions over broad domain explanations.
6. Make the research object explicit before the problem statement.
7. Explain normal and abnormal workflows when the research object is a security problem, fraud pattern, vulnerability, failure mode, or abuse behavior.
8. Use a running example only if it will help Methodology, Motivating Example, or Evaluation.
9. Keep notation and object names consistent with Methodology and Evaluation.

## Checklist

1. Are all concepts required by Methodology defined?
2. Is the running object or research object explicit?
3. Is the subject system or studied problem class clearly bounded?
4. Does the section explain the object's components, roles, or lifecycle when needed?
5. Is the task input/output or study target formalized?
6. Are assumptions and threat model stated before the method relies on them?
7. Does the section avoid unrelated background details?