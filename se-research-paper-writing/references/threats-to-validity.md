# Threats to Validity Writing Guide

## Goal

Use this standalone guide when Discussion has a dedicated Threats to Validity subsection or when the user asks specifically for validity analysis.

## Standard Structure

1. Construct validity: whether measurements, labels, tasks, or proxies capture the intended SE construct.
2. Internal validity: whether observed effects can be attributed to the proposed method, study design, or analyzed factor.
3. External validity: whether results generalize beyond studied projects, languages, tasks, participants, time periods, tools, or organizations.
4. Conclusion validity: whether statistical, qualitative, or interpretive conclusions are reliable.
5. Reliability/reproducibility: whether another researcher could repeat the study or reuse the artifact.
6. Ethical/security considerations: when human subjects, mined developer data, vulnerabilities, exploits, or generated code are involved.

## Writing Pattern

`[Threat] may affect [claim]. We mitigate this risk by [mitigation]. However, [remaining boundary], so our conclusion should be interpreted within [scope].`

## Tool Paper Threats

Discuss benchmark representativeness, oracle quality, implementation bugs, baseline fairness, configuration sensitivity, deployment assumptions, adversarial adaptation, and scalability limits.

## Empirical Study Threats

Discuss sampling bias, label noise, construct validity, coder disagreement, missing data, platform bias, participant bias, temporal validity, statistical power, and generalization boundaries.

## Checklist

1. Is every threat tied to a concrete claim?
2. Does every threat include mitigation and remaining boundary?
3. Are generic threats replaced with paper-specific risks?
4. Are Abstract and Introduction claims scoped according to these threats?
5. Is reproducibility addressed when artifacts or data are central?