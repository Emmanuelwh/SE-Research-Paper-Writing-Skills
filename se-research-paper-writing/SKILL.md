---
name: se-research-paper-writing
description: Improve software engineering research papers for top-tier SE conferences and journals, including ICSE, FSE, ASE, ISSTA, MSR, SANER, ICSME, TSE, TOSEM, EMSE, and JSS. Use when drafting or revising Abstract, Introduction, Background, Problem Statement, Threat Model, Motivating Example, Preliminary Study, Methodology, Evaluation, Discussion, Threats to Validity, Related Work, Conclusion, reviewer-facing self-review, contribution framing, claim-evidence alignment, Tool Paper presentation, or Empirical Study presentation.
---
# SE Research Paper Writing

## Overview

Use this skill to turn a software engineering research draft into a reviewer-friendly, evidence-backed paper. Prioritize clear task background, concrete problem severity, challenge-driven methodology, RQ/evaluation alignment, numerical evidence, threats-to-validity honesty, and practical/research implications.

## Core Workflow

1. Classify the paper as either a Tool Paper or an Empirical Study before rewriting.
2. Clarify the paper story before sentence-level edits: SE context -> problem severity -> prior-work limitations -> gaps/challenges -> methodology/study design -> evaluation/findings -> implications.
3. Build a contribution-RQ-evidence map before drafting major sections.
4. Load only the needed section guide in `references/`.
5. Rewrite paragraph-by-paragraph, keeping one paragraph for one message.
6. Run reverse outlining after each revised section.
7. Check every major claim in Abstract and Introduction against Methodology, Evaluation, Discussion, and Threats to Validity.
8. Run final adversarial review with `references/paper-review.md`.

## Global SE Writing Principles

1. Make the SE problem concrete: name the developer, maintainer, tester, researcher, security analyst, tool builder, organization, or user affected by the problem.
2. Distinguish task, background knowledge, motivating case, artifact, data source, subject system, participant population, metric, RQ, claim, and implication.
3. Treat challenges as load-bearing structure: every major challenge should be addressed by Methodology and evaluated by Evaluation.
4. Treat research questions as load-bearing structure for Empirical Studies: Methodology and Evaluation should answer them directly.
5. Use claim strength proportional to evidence strength; weaken causal, generality, and practical-impact claims when evidence is limited.
6. Prefer precise SE evidence over generic performance language: datasets, projects, commits, issues, pull requests, bugs, vulnerabilities, test cases, participants, tools, baselines, statistical tests, effect sizes, qualitative coding, and real-world validation.
7. Present threats to validity and discussion as part of scientific reasoning, not as apologetic afterthoughts.
8. Make artifacts and reproducibility visible when relevant: data, code, benchmarks, scripts, prompts, annotation protocols, and replication package.
9. Maintain terminology consistency across Abstract, Introduction, Background, Methodology, Evaluation, Discussion, Related Work, and Conclusion.
10. Write for skeptical reviewers who ask: why is this SE, why is it new, why is the design sound, why should I trust the evidence, and who benefits?

## Paragraph Clarity Check

Use this quick test whenever the user asks whether a paragraph flows or is clear.

1. Read as an external SE reviewer:
   - Does this paragraph have one explicit message?
   - Does the first sentence state that message?
   - Are key nouns self-contained and SE-specific enough?
   - Does each sentence connect to the previous one by cause, contrast, consequence, refinement, example, or evidence?
2. Run reverse outlining:
   - Write down the section thesis or RQ.
   - Write down each paragraph topic sentence.
   - Write down the evidence or reasoning under each paragraph.
   - Check mapping: topic sentence -> section thesis/RQ, and evidence -> topic sentence.
3. If flow is weak, add temporary transition phrases and section-role labels, revise the paragraph, then remove unnecessary scaffolding.

Source reference:

- `references/does-my-writing-flow-source.md`

## Section Guides

Load only the needed section file:

1. Abstract: `references/abstract.md`
2. Introduction: `references/introduction.md`
3. Background, Problem Statement, and Threat Model: `references/background.md`
4. Motivating Example or Preliminary Study: `references/motivating-example.md`
5. Methodology: `references/methodology.md`
   - Start with an overall overview.
   - Then write concrete subsections for modules, study phases, algorithms, data processing steps, or analysis components.
6. Evaluation: `references/evaluation.md`
   - Start with experimental setup.
   - Then organize results by each concrete RQ or evaluation question.
7. Discussion, Threats to Validity, and Limitations: `references/discussion.md`
8. Related Work: `references/related-work.md`
9. Conclusion: `references/conclusion.md`

Auxiliary guides:

- Standalone Threats to Validity details: `references/threats-to-validity.md`
- Paper review and pre-submission self-check: `references/paper-review.md`
- Paragraph clarity source: `references/does-my-writing-flow-source.md`
- Example bank index: `references/examples/index.md`
- Compatibility note for old Method prompts: `references/method.md`
- Compatibility note for old Experiments prompts: `references/experiments.md`

## Paper-Type Routing

Use only the two high-level paper types defined in `references/abstract.md`.

### Tool Paper

Use this route when the main contribution is a tool, system, technique, framework, detector, analyzer, repair method, benchmarked pipeline, or practical workflow support.

1. Abstract: follow `Context -> Gap -> Technique -> Evaluation -> Implication`.
2. Introduction: emphasize task background, problem severity, prior-work limitations, challenges, challenge-aligned methodology, numerical evaluation evidence, and contributions.
3. Background: define domain concepts, system model, problem statement, and threat model when needed.
4. Motivating Example: show why current tools fail and why the proposed workflow is necessary.
5. Methodology: begin with an overview, then explain components in workflow order with input/output relations and challenge mapping.
6. Evaluation: begin with experimental setup, then answer evaluation questions/RQs with datasets, baselines, metrics, numbers, ablations, scalability, case studies, and real-world evidence when available.
7. Discussion: discuss practical deployment, limitations, threats to validity, failure cases, and generalization boundaries.

### Empirical Study

Use this route when the main contribution is understanding, measuring, characterizing, explaining, or deriving implications from SE data, artifacts, developers, organizations, tools, or practices.

1. Abstract: follow `Context -> Gap -> Study -> Findings -> Implication`.
2. Introduction: emphasize background, severity, missing knowledge, RQs, study design, findings preview, and implications.
3. Background: define key concepts, study scope, problem statement, and any threat model or domain assumptions.
4. Motivating Example or Preliminary Study: use it to justify RQs, taxonomy design, measurement choices, or study motivation.
5. Methodology: begin with study overview, then explain data collection, sampling, labeling/coding, measurement, analysis method, and reproducibility.
6. Evaluation/Results: begin with setup and dataset summary, then answer each RQ with concrete findings, numbers, qualitative evidence, and statistical/interpretive support.
7. Discussion: derive implications for researchers/practitioners/tool builders, discuss threats to validity, and scope generalization.

## Execution Rules

1. Build a mini-outline before drafting prose.
2. For every major claim, ask: which RQ, experiment, analysis, table, figure, case study, or qualitative evidence supports it?
3. For Background, define only concepts needed later; do not turn it into a textbook.
4. For Motivating Example or Preliminary Study, show why the problem exists and why naive/current solutions fail; do not reveal all final results too early.
5. For Methodology, explicitly include an overview before detailed subsections.
6. For Evaluation, explicitly include experimental setup before RQ-specific results.
7. Avoid vague contribution labels such as `comprehensive`, `effective`, `novel`, or `practical` unless the paper defines and supports them.
8. Do not overclaim generality beyond the studied languages, projects, tasks, benchmarks, participants, incidents, organizations, or platforms.
9. Before finalizing, append and answer a reviewer-risk checklist covering SE relevance, novelty, methodological soundness, evidence strength, discussion/threats, reproducibility, and writing clarity.
10. Do not load all references at once; load only the specific guide needed for the current edit target.

## Output Contract

When asked to rewrite or draft sections, return:

1. A compact section outline with 3-7 bullets.
2. Revised paragraphs with explicit paragraph roles, such as context, problem, prior work, challenge, overview, component, RQ, evidence, implication, discussion, threat, or limitation.
3. A claim-evidence map using `Claim: ... | Evidence: ... | Status: supported/needs evidence/overclaimed`.
4. A challenge-method-evaluation map when the task involves Introduction, Methodology, or Evaluation: `Challenge/RQ: ... | Method/Study Design: ... | Evidence: ... | Threat/Boundary: ...`.
5. A short self-review checklist covering SE relevance, novelty, flow, terminology, unsupported claims, missing evidence, discussion/threats, and reviewer risks.