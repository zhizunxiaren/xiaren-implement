# MCP

## 一句话定义

MCP 是让 agent 通过统一协议访问外部工具、数据源和应用能力的接口层。

## 适用场景

- 让 agent 读取外部系统，例如 GitHub、Notion、数据库、浏览器、设计工具。
- 暴露受控工具能力，例如查询、创建、编辑、部署。
- 将个人或团队工作流纳入 agent harness。

## 工程关注点

- 权限最小化。
- 工具返回结果可解释。
- 错误信息可诊断。
- 写操作需要明确边界。
- 与本地文件、git、日志之间建立追踪关系。

## 常见误区

- MCP 越多越好。实际应优先接入高频、可验证、有清晰权限边界的工具。
- 把 MCP 当作万能自动化。它只是工具暴露层，仍需要 schema、workflow 和 verification。
- 忽略隐私和密钥管理。

## 相关页面

- [Harness Engineering](harness-engineering.md)
- [Skills](skills.md)

## 参考资料

- Karpathy LLM Wiki gist: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

