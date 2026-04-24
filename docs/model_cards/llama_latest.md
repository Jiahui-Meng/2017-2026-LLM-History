# Meta Llama 最新模型卡：Llama 4 Scout / Maverick

## 基本信息

- 最新公开开放权重主线：Llama 4 Scout 与 Llama 4 Maverick，均为 image-text-to-text MoE 模型。[S033: model card][S034: model card]
- 开放程度：开放权重、Hugging Face gated access，许可证为 Llama 社区/自定义许可元数据。[S033: model card][S034: model card]

## 模型结构（官方披露）

| field | Llama 4 Maverick | Llama 4 Scout |
|---|---|---|
| architecture family | llama4 image-text-to-text。[S033: model card] | llama4 image-text-to-text。[S034: model card] |
| dense/MoE | MoE。[S033: model card] | MoE。[S034: model card] |
| total params | HF metadata 约 401.6B；公开规格约 400B。[S033: model card][S012: context table] | 109B。[S034: model card][S012: context table] |
| active params | 17B public active naming。[S033: model card] | 17B public active naming。[S034: model card] |
| layers | 官方未披露。[S033: model card] | 官方未披露。[S034: model card] |
| hidden size | 官方未披露。[S033: model card] | 官方未披露。[S034: model card] |
| attention mechanism | 官方未披露。[S033: model card] | 官方未披露。[S034: model card] |
| positional encoding | 官方未披露。[S033: model card] | 官方未披露。[S034: model card] |
| experts/router | 128E；router/top-k 细节官方未披露。[S033: model card][S012: context table] | 16E；router/top-k 细节官方未披露。[S034: model card][S012: context table] |
| context window | 1M。[S012: context table] | 10M。[S012: context table] |
| tokenizer/vocab | 官方未披露。[S033: model card] | 官方未披露。[S034: model card] |
| modal encoder | 图像+文本输入；视觉编码器层数/hidden size 官方未披露。[S033: model card] | 图像+文本输入；视觉编码器层数/hidden size 官方未披露。[S034: model card] |
| output heads/modalities | 文本输出。[S033: model card] | 文本输出。[S034: model card] |
| reasoning/test-time structure | 官方未披露。[S033: model card] | 官方未披露。[S034: model card] |
| deployment formats | Hugging Face gated repo、推理平台、本地开放权重部署，受许可约束。[S033: model card] | Hugging Face gated repo、推理平台、本地开放权重部署，受许可约束。[S034: model card] |
| officially undisclosed | layers、hidden size、attention、positional encoding、tokenizer/vocab、vision encoder 细节、完整训练/后训练配方。[S033: model card] | layers、hidden size、attention、positional encoding、tokenizer/vocab、vision encoder 细节、完整训练/后训练配方。[S034: model card] |

## 推理/产品系统结构

Llama 4 的官方公开重点是 open-weight MoE、多模态输入和超长上下文。与 Meta Muse Spark 的产品 subagents 不同，Llama 4 模型卡不把 agent workflow 写成底层结构。[S011: Muse Spark][S033: model card][S034: model card]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。LMArena 可比较人类偏好，但不能补出 Llama 4 未披露的层数和 attention 结构。[S050: schema]

## 核心优势

开放权重、多模态、MoE、17B active naming，以及 Scout 的 10M context 和 Maverick 的 128E 规模。[S012: context table][S033: model card][S034: model card]

## 核心短板

相较 Kimi/Qwen/DeepSeek/GLM 的 config.json，Llama 4 gated model card 未公开层数、hidden size、attention、tokenizer/vocab 和视觉塔细节。[S027: config.json][S028: config.json][S030: config.json][S032: config.json]

## 与其他模型的关键区别

Llama 4 是少数同时公开 open-weight、MoE、17B active naming 与百万级/千万级 context 的主流模型；但结构可审计粒度低于 config 公开更完整的 Qwen、DeepSeek、Kimi、GLM。[S012: context table][S030: config.json][S032: config.json]

## 未公开信息

layers、hidden size、attention mechanism、positional encoding、tokenizer/vocab、vision encoder 细节、router/top-k、完整训练数据、优化器和后训练配方官方未披露。[S033: model card][S034: model card]

## claim-to-source map

- C006 -> S033, S034, S012
- C021 -> S033, S012
