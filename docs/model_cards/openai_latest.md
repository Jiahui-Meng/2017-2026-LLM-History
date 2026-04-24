# OpenAI 最新模型卡

- 最新模型名称：GPT-5.5；API 侧需同时跟踪 GPT-5.4。[S001: Intro][S003: Availability]
- 发布时间：GPT-5.5 于 2026-04-23 发布；GPT-5.4 于 2026-03-05 发布。[S001: header][S003: header]
- 开放程度：闭源，API/ChatGPT/Codex 受平台访问控制；GPT-5.5 源文称未在 API 当日发布。[S004: rollout]
- 架构：官方未披露参数规模、专家数、attention、tokenizer；GPT-5.5 Pro 是同一 underlying model 使用 parallel test-time compute 的设置。[S002: Introduction]
- 预训练：数据规模、优化器、硬件官方未披露；GPT-5 曾披露 Azure AI supercomputers，但不能自动外推到 GPT-5.5。[S001: Intro]
- 后训练：官方披露系统卡与预部署安全评估；具体 SFT/RLHF/RLVR 配方未披露。[S002: Introduction]
- 推理方式：GPT-5.4 支持 reasoning effort、computer use、tool search、web research、1M context；GPT-5.5 强调更强工具使用、检查工作与复杂任务。[S003: Computer use][S001: Intro]
- 微调/部署：闭源 API/ChatGPT/Codex；GPT-5.4 API 可用，GPT-5.5 API 当日未发布。[S003: Availability][S004: rollout]
- LMArena 最新表现：text_style_control 中 GPT-5.4-high 在 2026-04-17 快照列为 rank 9、rating 1481.6、votes 11568。[S051: rows]
- 核心优势：agentic coding、computer use、知识工作与工具生态。[S001: Intro][S003: Computer use]
- 核心短板：闭源架构不可审计；GPT-5.5 API 可用性和企业部署细节需持续更新。[S004: rollout]
- 与其他模型关键区别：相比开放权重 MoE，OpenAI 主要以产品系统、工具、test-time compute 和安全栈公开差异。[S001: Intro][S002: Introduction]
- 未公开信息：参数、激活参数、专家、训练 token、数据配比、优化器、tokenizer。
- claim-to-source map：C001->S001/S004；C002->S003；C014->S050。

