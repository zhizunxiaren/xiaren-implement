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

## [2026-05-10] review | principled-breakdown second pass

- 审阅 `inbox/principled-breakdown-skill-issues.md` 的第二轮新增问题。
- 统一“不适用/简化/正常/完整”和“小型/中型/大型”模板命名关系。
- 将“命令输出”改成更明确的“纯信息查询或单步命令执行”。
- 在 walkthrough 中补充按“小型任务”模板填充后的输出示例。

## [2026-05-10] rename | clarify-to-build skill

- 将 repo-local skill 从 `principled-breakdown` 重命名为 `clarify-to-build`。
- 将概念页从 `wiki/concepts/principled-breakdown.md` 重命名为 `wiki/concepts/clarify-to-build.md`。
- 将 issue 复查文件从 `inbox/principled-breakdown-skill-issues.md` 重命名为 `inbox/clarify-to-build-skill-issues.md`。
- 更新 `AGENTS.md`、`CLAUDE.md`、`wiki/index.md`、`wiki/collections/skill-collection.md` 和 skill 元数据。

## [2026-05-10] fix | clarify-to-build related pages

- 修正 `wiki/concepts/clarify-to-build.md` 的相关页面：补充关系说明，并加入 `Prompt Library`。
- 在 `Skills`、`Harness Engineering`、`AI Engineering Landing`、`Prompt Library`、`Vibe Coding` 中补充指向 `Clarify to Build` 的反向链接。

## [2026-05-10] review | clarify-to-build issue additions

- 审阅 `inbox/clarify-to-build-skill-issues.md` 新增的第 9、10 项。
- 将 `skills/clarify-to-build/SKILL.md` 中的“不适用或简化使用场景”拆成“不适用场景”和“输出粒度选择”。
- 扩展“操作原则”，说明什么是阻塞有效拆解的问题，并补充备份工具示例。

## [2026-05-10] review | clarify-to-build landing loop

- 删除 `inbox/clarify-to-build-skill-issues.md` 中关于 `agents/openai.yaml` 的争议项。
- 新增并修复第 11-15 项：追踪矩阵、关键问题停机规则、假设位置、保留/延后/删除裁剪结果、概念页同步。
- 更新 `skills/clarify-to-build/SKILL.md` 的中型/大型输出模板，使需求、功能、实施和验收形成可检查闭环。
- 更新 `wiki/concepts/clarify-to-build.md`，补充输出粒度与落地闭环。

## [2026-05-10] review | clarify-to-build checkability pass

- 新增并修复 `inbox/clarify-to-build-skill-issues.md` 第 16-19 项。
- 将第二轮第 6、7、8 项标记为已修复。
- 在 `skills/clarify-to-build/SKILL.md` 中为追踪矩阵增加 `R/F/S/V` 稳定编号规则。
- 将“简化后的范围”改为范围摘要，避免与“裁剪结果”重复。
- 区分“验证”与“验收检查”：前者是可用手段集合，后者是最终必须执行或满足的检查清单。

## [2026-05-10] review | clarify-to-build fifth pass

- 审阅并修复 `inbox/clarify-to-build-skill-issues.md` 第 20-22 项。
- 在中型模板中新增“轻量功能拆解”，为追踪矩阵的 `F` 编号提供来源。
- 补全中型输出粒度摘要，并在 walkthrough 中加入中型任务追踪矩阵片段。
