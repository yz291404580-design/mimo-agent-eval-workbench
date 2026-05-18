# mimo-agent-eval-workbench
A real-world AI Agent coding workflow benchmark for evaluating MiMo-V2.5 in engineering tasks.
#MiMo Agent 工程任务自动化评测工作台

一个面向个人开发者和小团队的 AI Agent 工程任务评测项目，用于把真实代码库中的需求、Bug、Issue 或文档任务转化为可复盘的 Agent 工作流，并记录模型在真实开发任务中的表现。

## 项目目标

当前开发者在使用 Codex、Cursor、Claude Code、OpenCode 等 Agent 编程工具时，通常只能凭主观体验判断一个模型是否“好用”。本项目希望建立一个更可验证的评测流程：

- 使用真实代码库任务，而不是只跑抽象 benchmark；
- 记录 Agent 从理解需求、修改代码、运行测试到生成报告的完整过程；
- 比较不同模型在长上下文代码理解、多轮调试、中文需求理解和成本控制上的表现；
- 将有效配置、失败案例和最佳实践整理为中文文档，帮助开发者评估 MiMo-V2.5 在 Agent 编程场景中的实际价值。

## 核心工作流

```mermaid
flowchart LR
  A["输入任务：Issue / Bug / 需求文档"] --> B["Planner Agent：阅读代码库并拆解任务"]
  B --> C["Coding Agent：修改代码和补充测试"]
  C --> D["Reviewer Agent：代码审查和风险检查"]
  D --> E["Test Agent：运行测试与复现验证"]
  E --> F["Report Agent：生成评测报告"]
