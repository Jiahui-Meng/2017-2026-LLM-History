# Kimi 最新模型卡

- 最新模型名称：kimi-k2.6。[S017: Model List]
- 发布时间：官方 model list 已推荐 K2.6；K2 系列将于 2026-05-25 停止维护。[S017: Model List]
- 开放程度：open-weight/API，K2 lineage Modified MIT。[S017: Model List]
- 架构：K2 lineage 为 1T total / 32B active MoE；K2.6 为 native multimodal，支持 visual/text input。[S018: Overview][S017: Model List]
- 预训练：K2 quickstart披露 K2 架构定位；K2.6 完整预训练细节需官方技术报告更新。[S018: Overview]
- 后训练：K2.6 支持 thinking/non-thinking、dialogue/Agent tasks；完整 SFT/RL 配方未在 model list 披露。[S017: Model List]
- 推理方式：256k context、thinking/non-thinking modes、agent tasks。[S017: Model List]
- 微调/部署：API 与开放权重；具体本地部署格式需 K2.6 model card 更新。
- LMArena 最新表现：kimi-k2-thinking-turbo 在 text_style_control 2026-04-17 rank 53、rating 1430.3、votes 47731。[S051: rows]
- 核心优势：长上下文、agentic coding、开放权重、成本优势。[S017: Model List]
- 核心短板：K2.6 细节需要完整技术报告；Modified MIT 有条件。
- 与其他模型关键区别：Kimi 把超大 MoE、长上下文、agent 工作流和开放权重结合。
- 未公开信息：K2.6 完整训练 token、专家路由细节、vision encoder 细节以官方报告为准。
- claim-to-source map：C009->S017/S018；C014->S050。

