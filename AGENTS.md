# xiaren-implement Agent Instructions

本仓库用于收录和沉淀用户在 vibe coding、harness engineering、skills、MCP、提示词工程，以及 AI 工程落地中的经验、提示词、思考和可复用模式。

## 强制安全规则

- 禁止批量删除文件或目录。不要使用 `del /s`、`rd /s`、`rmdir /s`、`Remove-Item -Recurse`、`rm -rf`。
- 需要删除文件时，只能一次删除一个明确路径的文件，例如 `Remove-Item "C:\path\to\file.txt"`。
- 如果需要批量删除文件，停止操作并请求用户手动删除。
- 所有带密钥、token、credential、secret、api key 的文件都不要提交 git。
- 提交前必须检查隐私文件和敏感信息。
- 涉及 UnrealEngine/UE 的项目或插件时，不要触发编译。

## 项目定位

这个项目不是普通代码仓库，而是一个面向 AI 工程实践的 LLM Wiki / personal engineering knowledge base。

它的目标是让经验持续复利：

- 把临时对话中的有效提示词沉淀成可复用资产。
- 把 skills、MCP、agent harness、工具链实践整理成结构化知识。
- 记录 vibe coding 与 harness engineering 的真实工程边界、失败模式和改进方法。
- 形成可检索、可交叉引用、可逐步演化的 markdown 知识库。

## 参考模式

本仓库采用 Andrej Karpathy 的 LLM Wiki 思路进行本地化落地：

- 原始资料层：用户收集的原始材料，LLM 只能读取和引用，不主动改写。
- Wiki 层：LLM 维护的结构化 markdown 页面，用于综合、归纳、交叉引用和更新。
- Schema 层：本文件 `AGENTS.md`，定义仓库结构、维护规则、入库流程、输出规范和安全边界。

参考链接：

- https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

## 目录职责

- `raw/`：原始资料。包括文章、导出的聊天、截图说明、论文、网页剪藏、工具文档片段等。此目录是事实来源，原则上只读。
- `raw/assets/`：原始资料引用的图片、截图和附件。
- `inbox/`：尚未整理的临时想法、待处理资料和对话摘录。
- `wiki/`：LLM 维护的综合知识库。
- `wiki/index.md`：内容索引。每次新增或修改 wiki 页面后都要更新。
- `wiki/log.md`：维护日志。记录 ingest、query、lint、refactor 等操作。
- `wiki/concepts/`：核心概念页，例如 vibe coding、harness engineering、MCP、skills。
- `wiki/collections/`：可复用资产集合，例如提示词库、skill 清单、MCP 清单、工程模式清单。
- `wiki/templates/`：入库、查询、复盘和总结模板。
- `skills/`：仓库内沉淀的 repo-local Codex skill。成熟后可以再复制或安装到全局 Codex skills。

## 维护协议

### Ingest：入库

当用户提供新资料或把文件放入 `raw/` / `inbox/` 后：

1. 先阅读资料，确认主题、来源、日期和可信度。
2. 生成或更新相关 wiki 页面。
3. 保留到原始资料的引用，不把二手总结当作一手事实。
4. 更新 `wiki/index.md`。
5. 追加 `wiki/log.md`。
6. 如果资料与旧页面矛盾，明确标注冲突，而不是静默覆盖。

### Query：查询与综合

回答关于本仓库知识的问题时：

1. 先查 `wiki/index.md`，再读相关页面。
2. 必要时回到 `raw/` 查原始资料。
3. 输出时区分事实、推断、建议和待验证事项。
4. 对有长期价值的回答，询问或判断是否需要沉淀回 `wiki/`。

### Lint：知识库体检

定期检查：

- 孤立页面。
- 概念重复或命名不一致。
- 缺少来源的强结论。
- 过期工具、模型、API 或 MCP 信息。
- 重要概念被多次提到但没有独立页面。
- index 与实际文件不一致。

## 写作规则

- 默认使用中文，必要时保留英文术语。
- 概念解释要面向学习者，说明背景、用途、边界和失败模式。
- 每个长期页面尽量包含：
  - 一句话定义。
  - 适用场景。
  - 不适用场景。
  - 操作方法或工程模式。
  - 常见误区。
  - 相关页面。
  - 参考资料。
- 不把聊天式结论直接堆进 wiki；需要重写成稳定知识。
- 不制造没有来源的确定性。如果只是当前理解，明确写成“当前判断”或“待验证”。

## 当前状态

- 2026-05-09：仓库初始化为 LLM Wiki 结构。
- 目前已有基础 schema、索引、日志、模板、初始概念页，以及第一个 repo-local skill `skills/principled-breakdown/`。
- 下一步应开始从用户已有提示词、skills、MCP 使用经验和 harness engineering 记录中逐条入库。
