# Tool Paper RQ Design Example

Use this example when deciding the Evaluation research questions for a Tool Paper.

## RQ Design Logic

Start from claims, not from available experiments.

| Paper Claim | Evaluation Need | Possible RQ |
| --- | --- | --- |
| The tool solves the main SE task | Measure primary task performance | RQ1 Effectiveness |
| The tool improves over current methods | Compare with SOTA/current practice | RQ1 or RQ2 Baseline Comparison |
| The method's modules are necessary | Remove/replace modules | RQ Ablation |
| The tool works in real settings | Test on real projects/cases | RQ Real-World Evaluation |
| The tool scales or is practical | Measure runtime/cost/user effort | Optional RQ Efficiency/Usability |

## Standard Tool Paper RQ Set

```text
We aim to address the following research questions:

RQ1 (Effectiveness): How effective is [Tool] in [main task] on [benchmark/dataset]?
RQ2 (Comparison): How does [Tool] compare with existing [tools/methods/current practice] under the same protocol?
RQ3 (Ablation): How much does each major component of [Tool] contribute to its performance?
RQ4 (Real-world applicability): Can [Tool] identify real [bugs/vulnerabilities/failures/issues] in real-world [projects/systems/ecosystems]?
```

## When to Merge Baseline Comparison into RQ1

Merge comparison into effectiveness when:

1. The same table answers both effectiveness and baseline comparison.
2. The main goal is simply to show better task performance.
3. There is no need for a separate deep analysis of baseline behavior.

Merged version:

```text
RQ1 (Effectiveness): How effective is [Tool] compared with existing methods on [main benchmark]?
RQ2 (Ablation): How much does each major component contribute to [Tool]'s effectiveness?
RQ3 (Real-world applicability): Can [Tool] find real [bugs/vulnerabilities/issues] in real-world [projects/ecosystems]?
```

## When to Keep SOTA Comparison Separate

Keep it separate when:

1. Existing methods are strong and deserve detailed analysis.
2. The paper claims a different capability, not only better scores.
3. Existing tools work well in some cases but fail in others.
4. The comparison includes multiple protocols, datasets, or adaptation details.

Separate version:

```text
RQ1 (Effectiveness): How accurately does [Tool] solve [main task]?
RQ2 (Comparison with existing methods): Where does [Tool] improve over SOTA methods, and where do existing methods remain competitive?
RQ3 (Ablation): Which modules are responsible for the improvement?
RQ4 (Real-world evaluation): Can [Tool] produce confirmed findings on real-world subjects?
```

## Security Tool Variant

```text
We aim to address the following research questions:

RQ1: How accurately does [Tool] detect [target vulnerability/bug/attack pattern] on curated benchmark cases?
RQ2: How does [Tool] compare with existing analyzers and auditing tools?
RQ3: How much do [module A], [module B], and [module C] contribute to detection performance?
RQ4: Can [Tool] discover previously unknown or unreported issues in real-world [projects/contracts/systems]?
RQ5: What are the main false positives and false negatives, and what do they reveal about the method's boundary?
```

## Checks

1. Does every RQ test one clear claim?
2. Is the first RQ the main effectiveness question?
3. Are ablation RQs tied to Methodology modules?
4. Is real-world evaluation included only if the paper can provide confirmation evidence?
5. Are optional RQs included because of claims, not because experiments are easy to run?