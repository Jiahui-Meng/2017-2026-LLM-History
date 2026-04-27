# OpenAI 家族发展史

## 家族主线

OpenAI 路线是 LLM 主线里最典型的“预训练扩展 -> 对齐 -> 产品化 -> 推理预算化”演进。

| 时间 | 节点 | 提升 | 创新 |
|---|---|---|---|
| 2018 | GPT-1 | 把生成式预训练做成统一迁移范式 | unsupervised generative pre-training。[S037] |
| 2020 | GPT-3 | few-shot 能力显著增强 | scaling 带来的 in-context learning。[S040] |
| 2022 | InstructGPT / ChatGPT | 更会遵循意图、对话更稳定 | RLHF 产品化。[S043] |
| 2023 | GPT-4 | 泛化和多模态能力跃升 | 更强系统级对齐与部署。[S044] |
| 2026 | GPT-5.4 / GPT-5.5 | 更强真实工作、工具与推理执行 | reasoning effort、computer use、1M context、Pro 路线。[S001][S002][S003][S004] |

## 每代的核心创新

- `GPT-1`：证明通用语言模型可以先预训练、再迁移，不必为每个任务单独造模型。[S037]
- `GPT-3`：把“规模本身就是方法”推成共识。[S040]
- `ChatGPT`：让 RLHF 从研究方法变成大众产品交互范式。[S043]
- `GPT-4`：把多模态与更强系统安全评估推进主流。[S044]
- `GPT-5.x`：把推理预算和工具工作流显式产品化，但底层结构继续官方未披露。[S001][S003]

## 当前最新节点

- `GPT-5.5` 是 OpenAI 最新公开 ChatGPT/Codex 旗舰之一；API 侧可审计主线仍需同时看 GPT-5.4。[S001][S003][S004]
- 官方公开重点是 reasoning、computer use、长上下文与真实工作表现，而不是参数规模。[S001][S002][S003]

## 仍未披露的信息

GPT-4、GPT-5.4、GPT-5.5 的 dense/MoE、参数规模、层数、专家路由、训练 token 和完整后训练配方均官方未披露。[S001][S002][S044]
