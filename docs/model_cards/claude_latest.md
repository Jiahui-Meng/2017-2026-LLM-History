# Claude 最新模型卡

- 最新模型名称：Claude Opus 4.7。[S005: header]
- 发布时间：2026-04-16。[S005: header]
- 开放程度：闭源，Claude products/API/Amazon Bedrock/Vertex AI/Microsoft Foundry 可用。[S005: Availability]
- 架构：官方称 hybrid reasoning model；参数、专家、attention、tokenizer 官方未披露。[S006: product page]
- 预训练：训练数据规模和硬件官方未披露。
- 后训练：官方披露安全评估、alignment assessment，并提到训练中实验性降低高风险 cyber 能力。[S005: Safety and alignment]
- 推理方式：xhigh effort、task budgets、Claude Code auto mode/ultrareview、高分辨率图像支持。[S005: Also launching today]
- 微调/部署：闭源 API 与云平台；未开放权重。[S005: Availability]
- LMArena 最新表现：text_style_control/latest 中 claude-opus-4-7-thinking rank 1、rating 1504.5、CI 1493.2-1515.9、votes 2618，票数仍低于 Opus 4.6 thinking。[S051: rows]
- 核心优势：长程编码、指令遵循、多步 agent、视觉细节。[S005: Testing][S005: Improved multimodal support]
- 核心短板：闭源不可审计；新模型 token usage/tokenizer 变化需迁移测试。[S005: Migrating]
- 与其他模型关键区别：Anthropic 更强调可控 effort、Claude Code 工作流、安全/对齐披露与 long-horizon autonomy。[S005: Also launching today]
- 未公开信息：参数、激活参数、专家、训练 token、完整数据配比、优化器。
- claim-to-source map：C003->S005/S006；C014->S050。

