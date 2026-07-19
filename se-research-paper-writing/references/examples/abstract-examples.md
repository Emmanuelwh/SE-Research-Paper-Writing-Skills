# Abstract Examples

Use these examples to learn abstract structure and sentence roles. They are condensed and anonymized from software engineering/security papers; do not reuse tool names, exact numbers, or original wording.

## Tool Paper Examples

### Tool Paper Example 1: Semantic Tracing for Complex Transaction Workflows

**Role map:** Context -> Gap -> Technique workflow -> Evaluation -> Implication.

`Decentralized financial applications create complex transaction workflows that make post-incident asset tracing difficult for investigators. Existing tracing tools often follow low-level transfer records or treat protocols uniformly, so they miss transaction intent and produce noisy paths when funds move through multiple protocols or chains. We propose a semantic-aware tracing framework that recovers high-level transaction meanings from raw blockchain activity. Given a transaction, the framework first extracts protocol-specific signals, then infers hidden financial intent through rule-guided and retrieval-assisted reasoning, converts the transaction into a compact semantic unit, and finally composes these units to update account states and expand the tracing frontier. We evaluate the framework on a large set of real-world laundering cases across single-chain and cross-chain settings, using destination accuracy, address coverage, and topology compactness as main measures. The results and case analysis show that semantic transaction modeling can reduce investigation noise and support continuous tracing across heterogeneous ledgers.`

**Reusable lesson:** For a Tool Paper abstract, the technique paragraph should expose the whole pipeline: raw input -> semantic inference -> intermediate representation -> iterative analysis -> final output.

### Tool Paper Example 2: Multi-View Detection of Malicious Token Behavior

**Role map:** Context -> Gap -> Technique workflow -> Evaluation -> Practical effect.

`Fraudulent token schemes remain a serious threat to decentralized finance because attackers can combine contract-level restrictions with market-level manipulation to trap investors. Existing detectors usually inspect either code patterns or transaction statistics, which makes them brittle when malicious behavior emerges from the interaction between implementation logic and trading activity. We propose a multi-view detection technique that jointly models code risk and token-flow behavior. The technique first extracts risk-relevant control and data-flow properties from contract code, then builds a behavioral graph from token transactions, and finally learns complementary representations from both views before fusing them for classification. We construct a manually validated dataset of malicious and benign token cases and evaluate the technique against existing detectors. The results show strong detection performance, and a deployment-style analysis further suggests that multi-view modeling can identify many suspicious tokens before major user losses occur.`

**Reusable lesson:** When the contribution fuses multiple evidence sources, name each source, explain the representation built from it, and state how the representations are combined.

## Empirical Study Examples

### Empirical Study Example 1: Benchmarking Security Analysis Tools

**Role map:** Context -> Gap -> Study design -> Findings by evaluation question -> Implication.

`Smart contract vulnerabilities continue to cause severe losses, motivating many static analysis tools for detecting security defects. However, comparing these tools remains difficult because existing taxonomies and benchmarks are often coarse, incomplete, or outdated, which can bias tool evaluation. We conduct an empirical study that first builds a fine-grained vulnerability taxonomy and then uses it to construct a broad benchmark covering diverse code patterns, vulnerability categories, and application scenarios. Using this benchmark, we evaluate multiple widely used static analyzers across detection coverage, false positives, and complementarity. The study finds that many vulnerability categories remain poorly detected, precision can be low even when recall appears acceptable, and combining tools reduces missed vulnerabilities but increases manual inspection burden. These findings provide guidance for benchmark design, tool improvement, and tool selection in smart contract security practice.`

**Reusable lesson:** For an Empirical Study abstract, make the taxonomy/benchmark/study artifacts part of the evidence chain, then organize results around evaluation questions rather than around tool names.

### Empirical Study Example 2: Characterizing Fraud Patterns and Detector Gaps

**Role map:** Context -> Gap -> Study design -> Findings -> Implication.

`Fraudulent behavior in decentralized finance damages users and weakens trust in the software ecosystem. Although prior work proposes datasets and detectors, the field still lacks a unified view of fraud variants, dataset coverage, and detector capability. We conduct a systematic empirical study by collecting evidence from research and industry sources, deriving a fine-grained taxonomy of fraud patterns, building an expanded labeled dataset, and evaluating representative detection tools. The results show that existing datasets cover only part of the known behavior space, tool effectiveness varies substantially across fraud types, and complex multi-step attacks are harder to detect than simple cases. These findings indicate that future security tools should evaluate against richer taxonomies, more diverse datasets, and compound attack scenarios rather than relying only on coarse labels.`

**Reusable lesson:** When the paper studies a field's coverage gap, the abstract should connect taxonomy -> dataset -> tool evaluation -> implications for future research and practice.

## Short Reusable Skeletons

### Tool Paper Skeleton

`[Context/problem severity]. Existing tools [gap], causing [consequence]. We propose [anonymized tool/technique], which [core idea]. Given [input], it first [step 1 and output], then [step 2 and output], and finally [step 3/final output]. We evaluate it on [dataset/tasks] through [main experiments] and [case study/real-world validation if available]. Results show [bounded evidence], suggesting [implication].`

### Empirical Study Skeleton

`[Context/problem severity]. Existing studies [gap], leaving [consequence]. We conduct [study type] on [dataset/artifacts/participants], covering [scope], to answer [RQs]. For RQ1, [finding]; for RQ2, [finding]; for RQ3, [finding]. These findings imply [guidance for researchers/practitioners/tool builders], while remaining scoped to [study boundary].`