# Mistral 最新模型卡：Mistral Large 3

## 基本信息

- 最新公开模型：Mistral Large 3，官方称其为 open-weight sparse MoE multimodal 模型。[S025: announcement][S026: docs]
- 开放程度：Apache 2.0 open-weight，并通过 Mistral AI Studio、Hugging Face 和多家云/推理平台分发。[S025: announcement][S026: docs][S035: model card]

## 模型结构（官方披露）

| field | Mistral Large 3 官方结构信息 |
|---|---|
| architecture family | Mistral Large 3 sparse MoE multimodal。[S025: announcement][S026: docs] |
| dense/MoE | Sparse MoE。[S025: announcement][S026: docs] |
| total params | 675B。[S025: announcement][S026: docs] |
| active params | 41B。[S025: announcement][S026: docs] |
| layers | 官方未披露。[S026: docs][S035: model card] |
| hidden size | 官方未披露。[S026: docs][S035: model card] |
| attention mechanism | 官方未披露。[S026: docs][S035: model card] |
| positional encoding | 官方未披露。[S026: docs][S035: model card] |
| experts/router | 官方披露 granular sparse MoE；专家数量、top-k、router 细节官方未披露。[S025: announcement][S026: docs] |
| context window | 256k context。[S026: docs] |
| tokenizer/vocab | 官方未披露。[S026: docs][S035: model card] |
| modal encoder | 图像理解能力公开；底层视觉编码器官方未披露。[S025: announcement][S026: docs] |
| output heads/modalities | 文本输出；多模态输入用于图像理解。[S025: announcement][S026: docs] |
| reasoning/test-time structure | 官方称 reasoning version coming soon；当前 Large 3 的内部 reasoning/test-time 结构官方未披露。[S025: announcement] |
| deployment formats | Mistral AI Studio、Hugging Face、Bedrock、Azure Foundry、OpenRouter、Fireworks、Together AI。[S025: announcement][S026: docs][S035: model card] |
| officially undisclosed | 层数、hidden size、attention、positional encoding、tokenizer/vocab、专家数量、router/top-k、完整训练与后训练配方。[S026: docs][S035: model card] |

## 推理/产品系统结构

Mistral Large 3 的公开结构重点是 open-weight sparse MoE 和 256k context；多平台部署是分发结构，不是内部模型结构。[S025: announcement][S026: docs]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。LMArena 分数不能补足未披露的专家路由或 attention 细节。[S050: schema]

## 核心优势

开放权重、Apache 2.0、675B/41B sparse MoE、256k context 和多平台可部署性。[S025: announcement][S026: docs]

## 核心短板

虽然开放权重，但官方文档未给出层数、hidden size、attention、tokenizer/vocab 与专家路由细节。[S026: docs][S035: model card]

## 与其他模型的关键区别

与 Qwen、DeepSeek、Kimi、GLM 的 config 级字段相比，Mistral Large 3 公开了规模和稀疏 MoE 总体设计，但结构粒度较粗。[S027: config.json][S028: config.json][S030: config.json][S032: config.json]

## 未公开信息

层数、hidden size、attention、positional encoding、tokenizer/vocab、专家数量、router/top-k、视觉编码器细节、完整训练和后训练配方官方未披露。[S026: docs][S035: model card]

## claim-to-source map

- C013 -> S025, S026
- C022 -> S025, S026, S035
