# 后训练路线演进

后训练决定模型“会不会按你的方式工作”。从 2021 到 2026，LLM 的可用性跃迁很大程度上都发生在这里。

## Instruction Tuning

- FLAN 把 instruction tuning 从技巧推进为清晰范式：让模型看见“任务是怎么被要求的”，zero-shot 任务表现会明显提升。[S042]
- 这一步为 chat、tool use、structured output 打下了接口层基础。

## RLHF

- InstructGPT 说明光靠 instruction tuning 还不够，模型还需要朝“人类更偏好的回答”继续优化。[S043]
- ChatGPT 则把 RLHF 的价值大规模产品化：回答更像助手，也更愿意拒绝不该做的内容。[S043]

## Constitutional AI

- Anthropic 把“让模型参考一套成文原则自我批评和修正”做成了与 RLHF 并列的重要对齐路线。[S045]
- 这条路线直接影响了 Claude 家族的安全风格、拒答方式和可控性叙事。[S045][S046][S047]

## Agentic Data 与 Reasoning RL

- DeepSeek-V3.2 披露了大规模 agent training data synthesis，并强调 thinking in tool-use。[S014]
- MiniMax-M2.1 披露了面向 coding、web explorer 和 long-horizon agent 的合成数据路线。[S021]
- DeepSeek-R1 把 reasoning-first RL 推成行业焦点之一，使“推理过程是否可训练”重新成为主问题。[S057]
- Claude 4.x、Gemini Thinking、OpenAI effort、Kimi thinking 说明后训练和推理时预算已经开始联动设计。[S003][S005][S009][S017]

## 现在的结论

1. 预训练决定“知道什么”，后训练决定“怎么工作”。
2. 2026 年的高端模型差异，很大一部分不再来自公开可见的参数规模，而来自后训练数据、奖励设计、推理预算和工具策略。
