# Wiki Log

按时间记录本 wiki 的维护动作。建议使用稳定前缀，方便后续检索。

## [2026-05-09] init | LLM Wiki scaffold

- 创建项目级 `AGENTS.md` schema。
- 创建 `raw/`、`inbox/`、`wiki/` 三层结构。
- 创建初始概念页、集合页、索引和模板。
- 项目定位为 vibe coding、harness engineering、skills、MCP、提示词和 AI 工程落地知识库。

## [2026-05-09] ingest | principled-breakdown skill

- 根据用户提出的“苏格拉底提问法 + 第一性原理 + 奥卡姆剃刀”组合想法，创建 repo-local skill `skills/principled-breakdown/SKILL.md`。
- 新增概念页 `wiki/concepts/principled-breakdown.md`。
- 更新 `wiki/index.md`、`wiki/collections/skill-collection.md` 和 `AGENTS.md`。

## [2026-05-09] refine | principled-breakdown Chinese maintenance version

- 将 `skills/principled-breakdown/SKILL.md` 改为中文主体，方便后续维护。
- 保留 frontmatter 中的英文触发关键词，避免降低 skill 触发覆盖。
- 将 `skills/principled-breakdown/agents/openai.yaml` 改为中文默认提示。

## [2026-05-09] review | principled-breakdown issue review

- 审阅 `inbox/principled-breakdown-skill-issues.md`。
- 接受“不适用场景”“规模对照”“提问库分组”“walkthrough 示例”四项反馈，并更新 `skills/principled-breakdown/SKILL.md`。
- 保留 `skills/principled-breakdown/agents/openai.yaml`，因为它是 skill-creator 推荐的 OpenAI UI 元数据；同步更新默认提示，但不扩展为完整 agent 配置。
