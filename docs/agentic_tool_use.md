# Agent 与工具使用演进

Agentic tool use 是 LLM 发展史里的后期主题。模型先学会说话，再学会按指令做事，最后才开始学会使用工具、验证结果、持续执行任务。

## 从 Chat 到 Tool Use

- ChatGPT 让对话成为主入口，但当时的工具系统仍相对有限。[S043]
- GPT-4 之后，function calling、code execution、search、computer use 逐渐进入主流接口。[S003][S044]

## 从 Tool Use 到 Long-Horizon Work

- Claude 4.x 明确强调 agentic coding、task budget 和长程执行。[S005][S047]
- Gemini 3 把 thinking、search grounding、code execution 和 multimodal 输入放进同一工作流。[S008][S009]
- GLM-5.1、MiniMax-M2.1、Kimi K2.6 都把 long-horizon task、tool use、agent 任务写进官方定位。[S017][S020][S022]
- DeepSeek-V3.2 的 thinking in tool-use 说明工具调用已不再只是外层编排，而在逼近模型的推理过程设计。[S014]

## 产品系统与 Base Model 的分界

- Muse Spark、ChatGPT、Claude Code、Gemini app 这类体验往往是模型、路由、权限、搜索、文件系统和安全策略的组合体。[S003][S011]
- 因此本项目把“产品系统节点”和“base model 节点”强制分开记录，避免把路由能力误写成底层架构能力。

## 现在的结论

1. agent 能力是模型能力、后训练、推理预算和工具系统共同作用的结果。
2. 到 2026 年，模型是否能“持续完成工作”比“单次回答像不像”更重要。
