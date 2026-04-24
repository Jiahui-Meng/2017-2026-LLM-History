# 架构 vs LMArena

## 可见关系

MoE 开放模型在 LMArena 上已经具备竞争力，例如 GLM、DeepSeek、Qwen、Mistral、MiniMax、Kimi 都进入 text_style_control 或 webdev 的可见排名区间。[S051: rows][S052: webdev latest] 这说明开放权重 MoE 不再只是“本地可用”，而是能在偏好榜上接近闭源产品。

## 不可见关系

闭源模型参数与架构未披露，因此不能把 GPT/Claude/Gemini/Grok 的高分归因于某种参数规模或专家数量。[S001: Intro][S005: Intro][S009: Model table][S024: API table]

## 更强解释变量

WebDev 高分往往更可能来自后训练、工具使用训练、前端审美偏好、测试时计算、agent 框架兼容、产品脚手架，而不仅是 base model MoE/dense 架构。[S020: Benchmarks][S023: Agentic Coding][S005: Testing]

