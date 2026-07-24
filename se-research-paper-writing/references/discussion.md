# Discussion, Threats to Validity, and Limitations Guide

## Goal

Use Discussion to interpret what the results mean, where the method or study can be used, what remains uncertain, and how threats to validity bound the claims.

## Recommended Structure

1. Main implications: explain what the results mean for researchers, practitioners, tool builders, or benchmark designers.
2. Practical deployment or adoption: discuss usability, cost, integration, automation, runtime, data requirements, or manual effort.
3. Failure cases and boundaries: explain when and why the approach/study may fail.
4. Threats to validity: cover construct, internal, external, conclusion validity, and reliability/reproducibility when applicable.
5. Ethical/security considerations: discuss responsible disclosure, user data, privacy, adversarial misuse, generated code risk, or sensitive artifacts when relevant.
6. Future work: state concrete next steps that follow from limitations.

## Discussion vs. Threats to Validity

Use Discussion for interpretation and implications. Use Threats to Validity for risks that may weaken the evidence or claims. If the paper combines them, keep the roles distinct with short subsection labels.

## Threat Writing Pattern

For each threat, write:

1. Threat: what could go wrong?
2. Affected claim: which claim may be weakened?
3. Mitigation: what did the paper do to reduce the risk?
4. Remaining boundary: what uncertainty remains?

## Discussion Writing Rules

1. Do not introduce unsupported new claims.
2. Do not hide major negative results.
3. Do not use generic threats that could fit any paper.
4. Tie every limitation to claim scope.
5. Turn failure cases into useful guidance when possible.

## Semi-Template

`The results suggest [implication] for [stakeholder]. This implication is useful because [reason], but it is bounded by [scope/condition]. In practice, [deployment/adoption issue] may affect [outcome]. We mitigate this concern by [mitigation], while [remaining limitation] remains an open problem.`

## Checklist

1. Are implications derived from results rather than promises?
2. Are deployment issues or practical costs discussed when relevant?
3. Are failure cases explained instead of hidden?
4. Are threats specific to the paper's dataset, method, metrics, participants, or setting?
5. Are Abstract and Introduction claims scoped according to these limitations?