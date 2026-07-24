# Introduction Examples

Use these examples to learn section roles and argument flow. They are condensed and anonymized from software engineering/security papers. Do not reuse original tool names, exact incident details, exact numbers, or original wording.

These examples are intentionally semi-templated. Some parts are written as concrete anonymized prose, while other parts use slots such as `[how they work]`, `[limitation]`, `[consequence]`, `[dataset scope]`, and `[main result]`. Fill the slots according to the user's paper instead of copying the example as a fixed paragraph.

## How to Use These Examples

1. Read `references/introduction.md` first.
2. Select the paragraph role you need: context, problem, prior work, challenges, methodology, evaluation, or contributions.
3. Reuse the rhetorical structure, not the domain-specific claims.
4. Replace bracketed slots with paper-specific facts, mechanisms, evidence, and numbers.
5. Keep every challenge aligned with a later methodology design.
6. Keep every evaluation number traceable to the paper's Evaluation section.

## Full Introduction Flow

A strong SE Introduction usually follows this chain:

`SE Context -> Problem Severity -> Prior Work and Current Practice -> Gaps and Challenges -> Methodology -> Evaluation -> Contributions`

The examples below show this flow using two anonymized paper patterns:

1. **Example A:** a semantic tracing tool for complex blockchain transaction investigations.
2. **Example B:** a multi-view detection tool for fraudulent token behavior.

## 1. SE Context Examples

### Example A: Incident Response and Transaction Tracing

`Blockchain platforms support increasingly complex financial applications, where users interact with [protocol examples] to perform [financial operations]. This openness enables [positive ecosystem effect], but it also creates [security/abuse opportunity]. After a security incident, investigators must [incident-response task], often across [addresses/protocols/chains]. This makes [target task] an important software engineering problem for [stakeholder].`

**Reusable lesson:** Keep the background concrete, but leave room to swap in the user's ecosystem, task, and stakeholder.

### Example B: Fraudulent Token Schemes

`Decentralized software ecosystems allow developers to [create/deploy/trade artifact] with limited centralized oversight. While this supports [innovation benefit], it also enables [fraud/abuse pattern]. In a typical scenario, [brief case pattern], causing [user/ecosystem harm]. Detecting such behavior is therefore important for [security goal/trust goal].`

**Reusable lesson:** Give a compact scenario rather than a complete case narrative. The scenario should teach why the task matters.

## 2. Problem Severity Examples

### Example A: Why Tracing Is Hard and Urgent

`The difficulty is that [target behavior] rarely appears as [simple observable pattern]. Attackers or faulty systems can [how they complicate the workflow], producing [noisy/intermediate artifacts] that obscure [true intent/state/cause]. If analysts follow [naive evidence] directly, they may [failure mode], leading to [consequence].`

**Reusable lesson:** Connect technical complexity to harm. Do not stop at `this is challenging`; name the consequence, such as wasted effort, false alarms, missed targets, delayed response, or unrecovered loss.

### Example B: Why Single-Signal Detection Is Risky

`[Target behavior] is difficult to detect because [malicious/faulty/undesired intent] may be expressed through [signal A], [signal B], or their interaction. Some cases rely mainly on [code/configuration/design signal], while others appear through [runtime/transaction/user behavior signal]. A method that observes only [one signal] can therefore [false negative mode] or [false positive mode].`

**Reusable lesson:** This pattern works when the problem has heterogeneous manifestations and incomplete observation is the central risk.

## 3. Prior Work and Current Practice Examples

### Example A: Existing Tracing Strategies

`Existing methods typically rely on [strategy A] or [strategy B]. [Strategy A] can recover [what it captures], but it does not explain [missing semantic layer]. For example, [complex workflow example] may involve [hidden operations], which are not visible from [low-level evidence] alone. Consequently, current methods may [bad downstream behavior], producing [consequence].`

**Reusable lesson:** State what prior work captures, what it misses, and why the missing piece hurts the task.

### Example B: Existing Detection Strategies

`Existing detectors often follow two lines of work. [Family A] searches for [risk pattern] and can [strength], but it may miss [case type] because [limitation]. [Family B] models [behavioral/statistical signal], but it may confuse [benign behavior] with [malicious behavior] when [missing context]. Because real cases may combine [signal A] and [signal B], methods that isolate either view have limited robustness.`

**Reusable lesson:** Use symmetric contrast when there are two prior-work families. The goal is not to defeat prior work cheaply, but to motivate your design space.

## 4. Gaps and Challenges Examples

### Example A: Challenge Decomposition for Semantic Tracing

`Addressing this gap requires solving [number] challenges. First, [C1: heterogeneity/semantic variation] is difficult because [why same observations may mean different things]. Second, [C2: implicit intent/hidden state] cannot be reliably recovered by [simple rule/baseline] because [reason]. Third, [C3: cross-context continuity] becomes difficult when [chains/projects/modules/organizations] do not expose [explicit link].`

**Reusable lesson:** A challenge should be a technical obstacle with a reason. Each challenge should prepare a method component later.

### Example B: Challenge Decomposition for Multi-View Detection

`A robust method must address [number] challenges. First, [phenomenon] evolves over time, making [fixed patterns/static rules] fragile. Second, [signal A] and [signal B] are complementary but not always co-occurring, so the method must [model separately] while also [learn interaction/fusion]. Third, [optional hard setting] requires [additional capability].`

**Reusable lesson:** Use placeholders to keep this adaptable. The user should replace `signal A/B` with code, transaction, log, prompt, test, configuration, or human-process evidence as needed.

## 5. Methodology Examples

### Example A: Methodology Paragraph for Semantic Tracing

`To address these challenges, we propose [name], a [tool/method/framework] for [target task]. Given [input], [name] first [step 1: explicit extraction], producing [output 1] to address [C1]. It then [step 2: inference/reasoning/normalization], which handles [C2]. For [hard setting], [name] [step 3], enabling [continuity/generalization]. Finally, it [step 4: composition/decision/report generation], producing [final output].`

**Reusable lesson:** Keep the workflow complete, but represent method internals as slots so the example does not overfit to one paper.

### Example B: Methodology Paragraph for Multi-View Detection

`To address these challenges, we propose [name], a [method/framework/tool] that integrates [view A] and [view B]. The method first [extracts/models view A] to capture [risk/semantic/property type]. In parallel, it [extracts/models view B] to characterize [behavior/process/context]. It then [fusion/decision mechanism] to combine [complementary evidence] for [final task].`

**Reusable lesson:** This pattern is useful whenever the contribution combines multiple representations, modalities, analyses, or evidence sources.

## 6. Evaluation Examples

### Example A: Evaluation Preview for Semantic Tracing

`To evaluate the effectiveness of [name], we curate/evaluate on [dataset], covering [dataset scope]. We compare [name] with [baseline family] using [metrics]. Experimental results show that [main result with numbers]. [Case study/real-world validation/ablation] further shows [practical or technical effect].`

**Reusable lesson:** This section should include concrete numbers in the final paper, but the example keeps `[main result with numbers]` as a slot so users supply paper-specific evidence.

### Example B: Evaluation Preview for Multi-View Detection

`To evaluate the effectiveness of [name], we construct/use [dataset] and compare it with [representative baselines]. Results show that [name] achieves [precision/recall/F1/other metrics] and improves over [baseline] by [number]. In [deployment-style analysis/case study/user study], [name] further [real-world effect].`

**Reusable lesson:** Combine benchmark evidence with practical evidence when available, but avoid inventing numbers.

## 7. Contribution Examples

### Example A: Contributions for Semantic Tracing

`The paper makes the following contributions:`

1. `We propose [name], a [tool/method/framework] for [target task], enabling [stakeholder] to [desired capability] in [target setting].`
2. `To address [challenge 1] and [challenge 2], we design [core abstraction/reasoning module/workflow], which [how it works] and [technical benefit].`
3. `We evaluate [name] on [dataset scope]. Experimental results show [main numerical evidence], and [case study/real-world validation] demonstrates [practical value].`

### Example B: Contributions for Multi-View Detection

`The paper makes the following contributions:`

1. `We conduct [empirical study/manual analysis/controlled experiment] on [dataset/artifacts/participants] to characterize [phenomenon], revealing [main insight].`
2. `We propose [name], a [method/framework/tool] that jointly models [view A] and [view B] to solve [target task].`
3. `To integrate complementary evidence, we design [representation/fusion/analysis component], which [how it works] and addresses [challenge].`
4. `We evaluate [name] on [dataset/task]. Experimental results show [main result], and [additional validation] further demonstrates [effect].`

## Short Reusable Skeletons

### SE Context Skeleton

`[SE ecosystem/workflow] has become important because [background knowledge]. In this setting, [stakeholder] must [task]. Recent cases or data show that [problem evidence], making [task] an important software engineering problem.`

### Problem Skeleton

`However, [task] remains difficult because [technical/practical reason]. This difficulty causes [harm], such as [consequence 1] and [consequence 2]. Therefore, [stakeholder] needs [capability/tool/study] to [desired outcome].`

### Prior Work Skeleton

`Existing approaches mainly rely on [strategy A] or [strategy B]. [Strategy A] can [strength], but fails to [limitation], leading to [consequence]. [Strategy B] addresses [aspect], but assumes [assumption] and therefore struggles with [target setting].`

### Challenge Skeleton

`Addressing this gap requires solving [number] challenges. First, [C1] is difficult because [reason]. Second, [C2] requires [capability], but [obstacle]. Third, [C3] becomes challenging when [hard setting].`

### Methodology Skeleton

`To address these challenges, we propose [name], a [tool/method/framework] that [main function]. Given [input], it first [step 1 and output] to address [C1], then [step 2 and output] to address [C2], and finally [step 3 and output] to address [C3/final goal].`

### Evaluation Skeleton

`To evaluate the effectiveness of [name], we evaluate it on [dataset], containing [scope]. Experimental results show that [name] achieves [metric/result] and outperforms [baseline] by [number]. [Case study/real-world validation/ablation] further shows [practical or technical effect].`