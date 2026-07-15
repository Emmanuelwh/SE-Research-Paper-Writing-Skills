# Skills: SE Research Paper Writing

本仓库提供一套面向软件工程研究论文写作的 Skill：

- `se-research-paper-writing/`
  - `SKILL.md`：核心工作流、使用规则和输出格式
  - `references/`：按章节拆分的软件工程论文写作指南
  - `agents/openai.yaml`：Codex 展示元信息

## 适用对象

该 Skill 面向准备投稿软件工程顶会/顶刊的作者，例如 ICSE、FSE、ASE、ISSTA、MSR、SANER、ICSME、TSE、TOSEM、EMSE、JSS 等。

## 典型用途

- 撰写或重写 Abstract、Introduction、Related Work、Methodology、Evaluation、Threats to Validity
- 设计 Research Questions，并建立 contribution-evidence map
- 检查论文中的 claim 是否被实验、实证数据、用户研究或案例研究支撑
- 按 reviewer 视角做投稿前自审
- 改善段落流畅性、术语一致性和审稿人可读性

## 安装方式

假设当前在仓库根目录。

### Codex

复制 Skill 到 `$CODEX_HOME/skills/`：

```bash
mkdir -p "$CODEX_HOME/skills"
cp -R se-research-paper-writing "$CODEX_HOME/skills/"
```

使用示例：

```text
Use $se-research-paper-writing to improve my ICSE paper introduction.
```

### Claude Code

全局安装：

```bash
mkdir -p "$HOME/.claude/skills"
cp -R se-research-paper-writing "$HOME/.claude/skills/"
```

项目级安装：

```bash
mkdir -p .claude/skills
cp -R se-research-paper-writing .claude/skills/
```

### Gemini

```bash
mkdir -p "$HOME/.gemini/skills"
cp -R se-research-paper-writing "$HOME/.gemini/skills/"
```

## 许可证

本项目采用 MIT License。详见 [LICENSE](./LICENSE)。
