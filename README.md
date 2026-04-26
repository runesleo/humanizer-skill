# Humanizer Skill

**English:** [README.en.md](./README.en.md)

---

单文件 Claude Code Skill：按维基百科「AI 写作迹象」框架识别并改写常见 AI 腔，并在去模板化同时强调节奏、观点与「人味」。

## When to use

- 需要**编辑或审校**自然语言，让读者觉得更像人写的、少模板感（与 `SKILL.md` frontmatter `when_to_use` 一致）。
- 成稿来自 LLM 辅助写作，要系统性扫一遍：夸大意义、促销腔、`-ing` 凑深度、模糊引用、AI 高频词、破折号滥用等 `SKILL.md` 中列出的模式。
- 需要在**保留原意**前提下压「客服腔」「知识截止免责声明」「空洞积极收尾」等沟通型 AI 痕迹。
- 希望走技能内建的流程：识别 → 改写 → 终稿前「还有哪些一眼 AI」的自查提示（见 `SKILL.md` Process）。

## When NOT to use

- 当前任务**不涉及**对读者面向的自然语言做「去 AI 痕迹 / 人格化」编辑时（与上述 `when_to_use` 相反；例如只产出机器可读配置、与文风无关的纯结构化数据）。
- 输入不是可编辑正文（无长文段落、无改稿对象）时，本 Skill 的「扫描—改写—终检」流程无从落地。
- 若你的流水线**无法**执行 `SKILL.md` 里要求的多段输出（草稿、自省、终稿等），应调整执行环境，而不是指望省略步骤仍达到同等审校深度（约束来自 `SKILL.md` Output format / Process）。

## Quick Start

1. 将本仓库中的 `SKILL.md` 放到 Claude Code 技能目录，例如 `~/.claude/skills/humanizer/SKILL.md`。
2. 或在项目内使用 `npx skills add`（若你的技能源已发布对应路径），再于对话中按技能说明调用。
3. 打开 `SKILL.md` 顶部的 `allowed-tools` 与正文流程，确认当前 Agent 具备所列工具权限。

## 典型场景

- 博客、 newsletter、产品文案在发布前做一轮「去 AI 腔」编辑。
- 把技术说明里泛滥的「关键 / 基石 / 生态系统」等统计高频词压成具体事实与短句。
- 对外文档中误粘贴的「希望有帮助」「当然！」等对话 artifacts 清理掉。
- 与团队「风格指南」配合：在保留术语表的前提下统一语气、减少加粗与 emoji 机械用法。

## 仓库结构（贡献者）

| 路径 | 说明 |
|------|------|
| `SKILL.md` | 唯一技能定义：frontmatter、24 类模式、流程与输出格式；改行为即改此文件。 |
| `LICENSE` | 许可证。 |
