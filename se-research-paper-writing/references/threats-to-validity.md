# Threats to Validity Writing Guide

## Goal

Write Threats to Validity as a precise account of what could weaken the claims, how the paper mitigates those risks, and which claims remain bounded.

## Standard Structure

1. Construct validity: whether measurements, labels, tasks, or proxies capture the intended SE construct.
2. Internal validity: whether observed effects can be attributed to the proposed method, study design, or analyzed factor.
3. External validity: whether results generalize beyond studied projects, languages, tasks, participants, time periods, tools, or organizations.
4. Conclusion validity: whether statistical, qualitative, or interpretive conclusions are reliable.
5. Reliability/reproducibility: whether another researcher could repeat the study or reuse the artifact.
6. Ethical considerations: when human subjects, mined developer data, vulnerabilities, or generated code are involved.

## Writing Pattern

For each threat, write:

1. Threat: what could go wrong?
2. Impact: which claim could be weakened?
3. Mitigation: what did the paper do to reduce the risk?
4. Boundary: what uncertainty remains?

## SE-Specific Threat Examples

1. Dataset bias: GitHub projects may not represent industrial systems.
2. Label noise: bug, vulnerability, or code-review labels may be incomplete or inconsistent.
3. Benchmark leakage: LLMs may have seen public benchmark data.
4. Oracle validity: generated tests, patches, or classifications may use imperfect ground truth.
5. Participant bias: survey/interview participants may not represent the broader developer population.
6. Tool implementation bias: engineering choices may affect performance independently of the core idea.
7. Temporal validity: repository behavior and tool ecosystems change over time.
8. Platform bias: GitHub/GitLab/Jira data reflect platform affordances and missing private communication.

## Rules

1. Do not write generic threats that could apply to any paper.
2. Do not use threats as a place to introduce new results.
3. Do not over-mitigate; acknowledge remaining uncertainty.
4. Tie each threat to a concrete claim, dataset, method, or evaluation choice.
5. Keep the tone honest and controlled: threats bound the contribution rather than destroy it.

## Checklist

1. Are construct/internal/external/conclusion validity covered when applicable?
2. Are SE-specific datasets, subjects, and metrics discussed?
3. Are LLM, human-subject, security, or repository-mining risks addressed when relevant?
4. Does each threat include mitigation and remaining boundary?
5. Are claims in Abstract/Introduction scoped according to the threats?
