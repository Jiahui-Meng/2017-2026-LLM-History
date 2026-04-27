# 推理模型演进

Reasoning model 不是单一技术名词，而是一条逐渐成形的路线：模型不仅要回答，还要更好地分解、验证、调用工具并坚持做完复杂任务。

## 从提示技巧到模型能力

- GPT-3 时代，复杂推理很大程度仍依赖 prompting 和示例设计。[S040]
- ChatGPT 时代，对话交互提升了可用性，但“深思熟虑”还不是独立产品能力。[S043]

## 从 GPT-4 到显式推理预算

- GPT-4 显示了更强的复杂任务能力，但推理时计算仍大多隐藏在产品后面。[S044]
- 到 GPT-5.x，OpenAI 已把 reasoning effort、Pro/parallel test-time compute 做成接口或产品能力的一部分。[S001][S002][S003]

## Claude、Gemini、Kimi、DeepSeek 的不同答案

- Claude 4.x：用 `effort` 和 `task budget` 把“愿意花多少计算做事”显式化，并和 coding agent 绑定。[S005][S047]
- Gemini 3：把 Thinking、grounding、function calling、code execution 组合成更完整的推理工作流。[S008][S009]
- Kimi K2.x：提供 thinking/non-thinking 路线，强调原生多模态和 agent 任务中的推理切换。[S017][S018]
- DeepSeek-R1 / V3.2：前者突出 reasoning RL，后者强调 thinking in tool-use，说明推理和工具正逐步融合。[S014][S057]

## 现在的结论

1. reasoning 不再只是“回答前多想几步”，而是和工具、预算、验证、长程执行一起设计。
2. 推理模型的真实竞争，已经从 benchmark 分数扩展到“能否持续完成一项真实工作”。
