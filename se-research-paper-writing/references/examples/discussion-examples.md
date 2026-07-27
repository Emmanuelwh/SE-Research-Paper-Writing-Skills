# Discussion and Threats to Validity Examples

Use this file after reading `references/discussion.md`. Threats to Validity is required and should use only External Validity and Internal Validity. Other discussion sections are optional.

## Minimal Combined Section

```latex
\section{Discussion and Threats to Validity}

\subsection{Discussion}
Our results suggest that [main implication] for [stakeholder]. This implication follows from [key result], where [Tool/Study] [summary of evidence]. In practice, [deployment/use issue] may affect adoption because [reason]. Therefore, we interpret the results as evidence for [bounded claim], not as evidence that [overclaim].

\subsection{Threats to Validity}
\textbf{External validity.} Our evaluation covers [evaluated scope], including [projects/datasets/tasks/ecosystems]. These subjects reduce the risk that results come from a single narrow setting. However, the results may differ for [unstudied languages/projects/organizations/workflows/threat models], so our generality claim is limited to [bounded scope].

\textbf{Internal validity.} Our results may be affected by [label quality/baseline configuration/metric choice/implementation detail/manual validation]. We mitigate this risk by [fixed protocol/manual inspection/multiple annotators/official implementation/repeated runs/artifact release]. Nevertheless, [remaining uncertainty] may remain, so the reported result should be interpreted as [bounded conclusion].
```

## External Validity Patterns

Use these as paragraph patterns inside the External Validity paragraph, not as extra headings.

- Dataset or project scope: `External validity concerns whether our results generalize beyond the evaluated projects. Our dataset covers [scope], including [diversity evidence]. However, it may not represent [unstudied ecosystems/languages/project sizes/domains]. We therefore limit our claim to [scope] and leave broader validation to future work.`
- Real-world deployment scope: `External validity may be affected by differences between our evaluation environment and real deployment. In practice, [input availability/user workflow/system configuration] may differ from our setting. We reduce this risk by evaluating [real-world subjects/scenarios], but the results should be interpreted as applying to settings where [assumption] holds.`
- Security or reliability scope: `External validity is limited by the evaluated [bug/vulnerability/failure] types. Although our subjects include [coverage], attackers, systems, or operational environments may exhibit [unstudied behavior]. Thus, our results support claims about [studied threat model/scope], not all possible [attacks/failures].`

## Internal Validity Patterns

Use these as paragraph patterns inside the Internal Validity paragraph, not as extra headings.

- Ground truth and manual validation: `Internal validity may be affected by errors in ground truth construction. We mitigate this risk by [manual validation/reproduction/two-author labeling/adjudication/developer confirmation]. However, some cases may remain ambiguous, so our conclusions about [metric/result] should be interpreted within this verification protocol.`
- Baseline fairness: `Internal validity may be affected by how baselines are configured. We reduce this risk by using [official implementation/default settings/same dataset/same timeout/same preprocessing]. Still, different configurations could change baseline performance, so our comparison should be interpreted under the stated protocol.`
- Metric or proxy choice: `Internal validity may be affected by using [metric/proxy] to measure [construct]. This metric captures [aspect] but may miss [missing aspect]. We mitigate this threat by also reporting [additional metric/manual analysis/case study]. Therefore, our conclusion concerns [bounded construct] rather than [broader construct].`
- Implementation and reproducibility: `Internal validity may be affected by implementation errors or nondeterminism. We mitigate this risk through [tests/code review/repeated runs/fixed seeds/artifact release]. Nevertheless, [remaining source of nondeterminism] may affect individual outputs, so we focus our conclusion on [stable aggregate/result].`

## Optional Discussion Patterns

These are optional sections outside Threats to Validity.

- Implication paragraph: `The results suggest [implication] for [stakeholder]. This implication follows from [specific result]. For practitioners, it means [actionable meaning]. For researchers, it suggests [research meaning]. We interpret this implication within [scope], because [boundary].`
- Practical deployment paragraph: `Deploying [Tool] requires [input/resources/workflow]. In our evaluation, [runtime/manual effort/output format] suggests that [deployment claim]. However, users should interpret [output] with [caution], especially when [failure condition].`
- Limitation paragraph: `[Tool/Study] currently does not address [setting/case]. This limitation arises because [reason]. It may affect [claim] when [condition]. Addressing it would require [future direction].`
- Ethical or security paragraph: `Because this work involves [vulnerabilities/developer data/generated code/sensitive artifacts], we [responsible action]. We avoid [risk] by [mitigation]. The released artifact will [release boundary], which balances reproducibility with [safety/privacy].`

## Common Fixes

1. If threats are split into construct, conclusion, reliability, or reproducibility headings, fold them into Internal Validity.
2. If a threat is about generalization beyond the evaluated scope, move it to External Validity.
3. If a threat does not name an affected claim, add the claim.
4. If a threat only says `may affect results`, add mitigation and remaining boundary.
5. If Discussion repeats Evaluation numbers, replace repetition with interpretation and implications.
6. If Limitations duplicates Threats, keep method boundaries in Limitations and evidence risks in Threats.