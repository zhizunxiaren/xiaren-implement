# Harness Engineering

## 一句话定义

Harness engineering 是围绕 AI agent 的执行环境进行工程化设计：上下文如何进入、工具如何暴露、权限如何限制、过程如何记录、结果如何验证。

## 适用场景

- 构建本地 coding agent 工作流。
- 设计 skills、MCP、CLI、测试和自动化之间的协作边界。
- 把一次性 AI 能力变成可重复、可审计的执行流程。
- 需要长期沉淀项目规则、上下文和操作规程的工程。

## 核心对象

- Agent：执行任务的模型和运行时。
- Context：项目规则、历史、源码、文档、用户意图。
- Tools：shell、浏览器、MCP、API、文件系统、测试命令。
- Policy：权限、安全边界、禁止动作、审批规则。
- Verification：测试、截图、日志、diff、人工验收。
- Memory：可复用的项目知识、技能、规范和经验。

## 工程模式

- 用 `AGENTS.md` 记录项目级规则，而不是把规则留在聊天里。
- 用 skills 固化重复工作流，例如调试、测试、发布、文档维护。
- 用 MCP 暴露外部系统，但保持权限最小化。
- 用日志和索引让知识库可追踪、可恢复。
- 用验证命令和验收标准约束 AI 的完成声明。

## 常见误区

- 只关注模型能力，不设计工具和权限边界。
- 只做 RAG 检索，不维护长期综合知识。
- 把所有自动化都做成黑盒，缺少日志和回滚。
- 没有区分原始资料、综合知识和执行规则。

## 相关页面

- [MCP](mcp.md)
- [Skills](skills.md)
- [Clarify to Build](clarify-to-build.md)
- [AI Engineering Landing](ai-engineering-landing.md)

## 参考资料

- Karpathy LLM Wiki gist: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
