# Related Work Writing Guide

## Goal

Write Related Work as an argument for the paper's position, not a bibliography dump. The section should show how the paper differs from and builds on prior SE research.

## Workflow

1. Identify 2-4 comparison axes that matter for the paper.
2. Group papers by problem, technique, evidence type, or SE workflow stage.
3. For each group, explain what prior work established and what remains missing.
4. End each subsection by connecting the gap to this paper's contribution.

## Organization Patterns

### By Problem Area

Use when the paper addresses a broad SE problem such as testing, debugging, maintenance, vulnerability detection, code review, or developer productivity.

### By Technique

Use when the main novelty is a method, such as static analysis, dynamic analysis, search-based SE, program repair, repository mining, or LLM-based automation.

### By Evidence Type

Use when the paper's value is empirical: surveys, interviews, mining studies, controlled experiments, replications, benchmarks, or mixed-methods evidence.

### By Workflow Stage

Use when the paper supports a specific development lifecycle stage: requirements, design, implementation, review, testing, deployment, maintenance, or incident response.

## Paragraph Template

1. Topic sentence: `A first line of work studies ...`
2. Synthesis: summarize shared assumptions, techniques, or findings.
3. Limitation/gap: explain what is missing relative to the paper's problem.
4. Positioning: state how this paper differs or complements the line of work.

## Comparison Table Guidance

Use a comparison table only when it clarifies dimensions reviewers care about, such as task, data source, supported language, evaluation subject, artifact availability, and threat model. Do not include a table that only marks checkboxes without explaining why the dimensions matter.

## Checklist

1. Does each subsection have a clear comparison axis?
2. Are papers synthesized rather than listed one by one?
3. Does the section avoid unfairly weakening prior work?
4. Are differences stated precisely without overclaiming novelty?
5. Does the final positioning make the paper's gap feel inevitable?
