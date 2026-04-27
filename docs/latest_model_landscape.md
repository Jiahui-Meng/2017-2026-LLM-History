# 当前格局快照

本页是附录，只回答“站在 2026 年回头看，现在这一代模型的竞争焦点是什么”，不再承担项目主线。

## 当前时代的三个中心矛盾

1. `闭源前沿模型` 主要在推理预算、工具系统和长程执行上竞争，而不是公开比拼参数规模。[S001][S005][S009][S024]
2. `开放权重前沿模型` 主要在 MoE、长上下文、部署效率和许可策略上竞争。[S014][S017][S019][S020][S022][S025]
3. `产品系统模型` 越来越不能只看 base model；搜索、代码执行、文件系统、computer use、subagents 往往决定最终体验。[S003][S011][S022]

## 当前最强的公开趋势

- MoE 已从 Mixtral 时代的“高效选择”发展为 DeepSeek、Qwen、Kimi、MiniMax、GLM、Llama 4、Mistral Large 3 的主流路线之一。[S014][S019][S020][S022][S025][S033]
- 长上下文不再只是 Gemini 的招牌，GPT-5.4、Claude Opus 4.7、Grok 4.20、Kimi K2.6、GLM-5.1 都把它推进到产品层接口。[S003][S006][S017][S022][S024]
- reasoning 被显式产品化：OpenAI 的 effort/Pro、Claude 的 xhigh effort、Gemini Thinking、Kimi thinking、DeepSeek-R1 与 V3.2 tool-use thinking 都在说明 test-time compute 已成为一等能力。[S003][S005][S009][S014][S017][S057]

## 如何和主时间线配合阅读

- 想看“为什么会走到今天”，先读 [全局时间线](llm_timeline.md)。
- 想看“谁把哪条路线做成主流”，读各家 [家族历史页](model_cards/openai_history.md)。
- 想看“MoE、RLHF、Constitutional AI、reasoning RL 到底是什么”，读专题页。
