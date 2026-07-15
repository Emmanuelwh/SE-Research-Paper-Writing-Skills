# Skills: SE Research Paper Writing

[中文介绍](./README_zh.md).

This repository provides one Codex-compatible skill package for software engineering research paper writing:

- `se-research-paper-writing/`
  - `SKILL.md`: core workflow, usage rules, and output contract
  - `references/`: section-specific writing guides for SE papers
  - `agents/openai.yaml`: UI metadata

## Intended Users

Use this skill when preparing papers for software engineering conferences and journals such as ICSE, FSE, ASE, ISSTA, MSR, SANER, ICSME, TSE, TOSEM, EMSE, and JSS.

## Typical Use Cases

- Drafting or rewriting Abstract, Introduction, Related Work, Methodology, Evaluation, and Threats to Validity
- Designing research questions and contribution-evidence maps
- Checking whether claims are supported by experiments, empirical data, user studies, or case studies
- Reviewing a paper from a skeptical SE reviewer perspective before submission
- Improving paragraph flow, terminology consistency, and reviewer-facing presentation

## Installation

Assume you are in the repository root.

### Codex

Copy the skill into `$CODEX_HOME/skills/`:

```bash
mkdir -p "$CODEX_HOME/skills"
cp -R se-research-paper-writing "$CODEX_HOME/skills/"
```

Usage example:

```text
Use $se-research-paper-writing to improve my ICSE paper introduction.
```

### Claude Code

Global:

```bash
mkdir -p "$HOME/.claude/skills"
cp -R se-research-paper-writing "$HOME/.claude/skills/"
```

Project-level:

```bash
mkdir -p .claude/skills
cp -R se-research-paper-writing .claude/skills/
```

### Gemini

```bash
mkdir -p "$HOME/.gemini/skills"
cp -R se-research-paper-writing "$HOME/.gemini/skills/"
```

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE).
