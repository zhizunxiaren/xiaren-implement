# Vibe Coding

## 一句话定义

Vibe coding 是一种以 AI 协作为主线、通过快速描述意图、观察结果、迭代修正来推进实现的编码方式。

## 适用场景

- 原型探索。
- UI 或交互快速试错。
- 不确定方向下的方案比较。
- 小工具、脚本、demo、知识库自动化。
- 已有工程中边界清晰的小功能。

## 不适用场景

- 安全关键系统。
- 需求尚未澄清但失败成本很高的核心模块。
- 缺少测试和验收标准的大规模重构。
- 涉及密钥、隐私、生产数据且没有权限边界的任务。

## 工程要点

- 先说明目标和边界，再让 AI 生成代码。
- 给 AI 提供真实目录、文件、错误信息和验收方式。
- 用小步提交或小步验证降低偏差。
- 对复杂任务建立 plan、tests、logs，而不是只靠聊天上下文。
- 把成功提示词沉淀到提示词库，把失败模式沉淀到复盘页。

## 常见误区

- 把“跑起来”误认为“工程可维护”。
- 没有保存关键提示词，导致经验不能复用。
- 没有验证，只看 AI 的完成声明。
- 一次性给过大任务，导致上下文漂移和错误堆叠。

## 相关页面

- [Clarify to Build](clarify-to-build.md)
- [Harness Engineering](harness-engineering.md)
- [Prompt Library](prompt-library.md)
- [AI Engineering Landing](ai-engineering-landing.md)

## 参考资料

- Karpathy LLM Wiki gist: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
