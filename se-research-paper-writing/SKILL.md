---
name: se-research-paper-writing
description: Improve software engineering research papers for top-tier SE conferences and journals, including ICSE, FSE, ASE, ISSTA, MSR, SANER, ICSME, TSE, TOSEM, EMSE, and JSS. Use when drafting or revising Abstract, Introduction, Related Work, Methodology, Evaluation, Threats to Validity, reviewer-facing self-review, research questions, contribution framing, claim-evidence alignment, empirical study design, tool/system paper presentation, or SE paper rebuttal preparation.
---
# SE Research Paper Writing

## Overview

Use this skill to turn a software engineering research draft into a reviewer-friendly, evidence-backed paper. Prioritize clear problem framing, SE-specific contribution claims, research-question alignment, methodology transparency, evaluation soundness, threats-to-validity honesty, and practical/research implications.

## Core Workflow

1. Classify the paper type before rewriting: empirical study, tool/system paper, program analysis/testing/verification paper, mining software repositories paper, LLM4SE/AI4SE paper, SE4AI paper, or security-for-SE paper.
2. Clarify the paper story before sentence-level edits: software engineering problem -> gap in existing knowledge/tools -> key insight or artifact -> evidence -> implications.
3. Build a contribution-RQ-evidence map before drafting major sections.
4. Load only the needed section guide in `references/`.
5. Rewrite paragraph-by-paragraph, keeping one paragraph for one message.
6. Run reverse outlining after each revised section.
7. Check every major claim in Abstract and Introduction against Methodology, Evaluation, and Threats to Validity.
8. Run final adversarial review with `references/paper-review.md`.

## Global SE Writing Principles

1. Make the SE problem concrete: name the developer, maintainer, tester, researcher, tool builder, or organization affected by the problem.
2. Distinguish task, setting, artifact, data source, subject system, participant population, metric, and claim.
3. Treat research questions as load-bearing structure: Methodology and Evaluation should answer them directly.
4. Use claim strength proportional to evidence strength; weaken causal, generality, and practical-impact claims when evidence is limited.
5. Prefer precise SE evidence over generic performance language: datasets, projects, commits, issues, pull requests, bugs, vulnerabilities, test cases, participants, tools, baselines, statistical tests, effect sizes, and qualitative coding.
6. Present threats to validity as part of the scientific contribution, not as an apology at the end.
7. Make artifacts and reproducibility visible when relevant: data, code, benchmarks, scripts, prompts, annotation protocols, and replication package.
8. Maintain terminology consistency across RQs, contributions, method, evaluation, figures, tables, and threats.
9. Write for skeptical reviewers who ask: why is this SE, why is it new, why is the design sound, why should I trust the evidence, and who benefits?

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

- Abstract: `references/abstract.md`
- Introduction: `references/introduction.md`
- Related Work: `references/related-work.md`
- Methodology: `references/methodology.md`
- Evaluation: `references/evaluation.md`
- Threats to Validity: `references/threats-to-validity.md`
- Conclusion: `references/conclusion.md`
- Paper review: `references/paper-review.md`
- Paragraph clarity source: `references/does-my-writing-flow-source.md`
- Example bank index: `references/examples/index.md`

## Paper-Type Routing

1. Empirical study: emphasize RQs, dataset/participant sampling, measurement validity, qualitative/quantitative analysis, and implications.
2. Tool/system paper: emphasize user problem, design goals, architecture, implementation, evaluation tasks, comparison to tools, and artifact availability.
3. Program analysis/testing/verification paper: emphasize formal problem, assumptions, algorithm/design, soundness tradeoffs, benchmarks, baselines, and failure cases.
4. MSR paper: emphasize repository selection, data extraction, cleaning, operationalization, sampling bias, statistical analysis, and replication.
5. LLM4SE/AI4SE paper: emphasize task definition, prompt/model setup, data leakage control, baselines, human evaluation, reliability, and reproducibility.
6. Security-for-SE paper: emphasize threat model, vulnerability/attack setting, dataset validity, detection/repair precision, and responsible disclosure when relevant.

## Execution Rules

1. Build a mini-outline before drafting prose.
2. For every major claim, ask: which RQ, experiment, analysis, table, figure, or qualitative evidence supports it?
3. For Methodology and Evaluation, explicitly include subject selection, data collection, procedure, metrics, baselines/comparisons, analysis method, and reproducibility details when applicable.
4. Avoid vague contribution labels such as "comprehensive", "effective", "novel", or "practical" unless the paper defines and supports them.
5. Do not overclaim generality beyond the studied languages, projects, tasks, benchmarks, participants, or organizations.
6. Before finalizing, append and answer a reviewer-risk checklist covering novelty, SE relevance, methodological soundness, evidence strength, threats to validity, reproducibility, and writing clarity.
7. Do not load all references at once; load only the specific guide needed for the current edit target.

## Output Contract

When asked to rewrite or draft sections, return:

1. A compact section outline with 3-7 bullets.
2. Revised paragraphs with explicit paragraph roles, such as opening, problem, gap, insight, contribution, RQ, methodology, evidence, implication, or limitation.
3. A claim-evidence map using `Claim: ... | Evidence: ... | Status: supported/needs evidence/overclaimed`.
4. An RQ alignment map when the task involves Methodology or Evaluation: `RQ: ... | Method: ... | Evidence: ... | Threat: ...`.
5. A short self-review checklist covering SE relevance, novelty, flow, terminology, unsupported claims, missing evidence, threats to validity, and reviewer risks.
