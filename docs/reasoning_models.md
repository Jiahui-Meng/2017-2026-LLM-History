# Reasoning Models

Reasoning model 的“能力”至少来自四层：

1. 预训练形成的基础世界模型与代码/数学能力。
2. 后训练让模型学会分解、验证、工具调用和拒答策略。
3. 推理时计算提供更长思考、并行 test-time compute 或 effort 控制。
4. 产品系统提供搜索、文件、电脑、代码执行、路由和权限。

OpenAI GPT-5.5 Pro 被 system card 描述为同一 underlying model 使用 parallel test-time compute 的设置。[S002: Introduction] Claude Opus 4.7 新增 xhigh effort 与 task budgets。[S005: Also launching today] Gemini 3 Pro Preview 支持 Thinking。[S009: Model table] Kimi K2.6 支持 thinking/non-thinking modes。[S017: Model List] GLM-5.1 支持 thinking mode 并定位 long-horizon autonomous tasks。[S022: Overview]

