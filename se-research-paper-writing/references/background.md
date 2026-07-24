# Background, Problem Statement, and Threat Model Guide

## Goal

Write this section so reviewers have the minimum domain knowledge needed to understand the problem, methodology, and evaluation. Use Background for concepts, Problem Statement for the formal task, and Threat Model for security/adversarial assumptions when relevant.

## When to Include This Section

Include a standalone Background section when the paper depends on domain concepts that are not obvious to a general SE reviewer, such as blockchain execution, compiler internals, program analysis abstractions, testing workflows, developer processes, LLM prompting pipelines, or security assumptions.

Include Problem Statement when the paper needs a precise task definition, inputs/outputs, assumptions, scope, or objective.

Include Threat Model when the paper involves security, abuse, adversaries, attacks, vulnerabilities, fraud, malware, privacy, or misuse.

## Recommended Structure

1. Background concepts: define only concepts used later.
2. Running objects: define subject systems, artifacts, entities, or actors.
3. Problem statement: define task, input, output, scope, and objective.
4. Threat model or assumptions: define adversary capability, trusted components, out-of-scope cases, and defender goal.
5. Bridge sentence: explain how this background prepares the motivating example, methodology, or evaluation.

## Background Writing Rules

1. Do not write a textbook survey.
2. Define terms before using abbreviations or custom terminology.
3. Prefer task-relevant definitions over broad domain explanations.
4. Use small examples when a definition is hard to understand.
5. Keep notation consistent with Methodology and Evaluation.

## Problem Statement Pattern

`Given [input/artifact/context], the goal is to [task/output] under [assumptions/scope]. A correct/effective solution should [requirement 1], [requirement 2], and [requirement 3]. We focus on [scope] and leave [out-of-scope case] to future work/discussion.`

## Threat Model Pattern

`We consider an adversary who can [capability] but cannot [constraint]. The defender observes [available evidence] and aims to [defender goal]. We assume [system/data/protocol assumption]. This threat model excludes [out-of-scope case], which we discuss in [Discussion/Threats to Validity].`

## Checklist

1. Are all concepts required by Methodology defined?
2. Is the task input/output clear?
3. Are scope boundaries explicit?
4. Are assumptions and threat model stated before the method relies on them?
5. Does the section avoid unrelated background details?