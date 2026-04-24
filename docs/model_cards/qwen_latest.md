# Qwen 最新模型卡：Qwen3.5-397B-A17B / Qwen3.6-35B-A3B

## 基本信息

- 最新公开结构样本：Qwen3.5-397B-A17B 与 Qwen3.6-35B-A3B，均为 `Qwen3_5MoeForConditionalGeneration` image-text-to-text 模型。[S019: repository][S030: config.json][S031: config.json]
- 开放程度：开放权重；HF config 公开 text_config 与 vision_config。[S030: config.json][S031: config.json]

## 模型结构（官方披露）

| field | Qwen3.5-397B-A17B | Qwen3.6-35B-A3B |
|---|---|---|
| architecture family | `Qwen3_5MoeForConditionalGeneration`。[S030: config.json] | `Qwen3_5MoeForConditionalGeneration`。[S031: config.json] |
| dense/MoE | MoE。[S030: config.json] | MoE。[S031: config.json] |
| total params | HF metadata 约 403,397.9M。[S030: config.json] | HF metadata 约 35,951.8M。[S031: config.json] |
| active params | A17B 为官方型号名；config 公开 `num_experts_per_tok=10`。[S030: config.json] | A3B 为官方型号名；config 公开 `num_experts_per_tok=8`。[S031: config.json] |
| layers | text 60 层；vision 27 层。[S030: config.json] | text 40 层；vision 27 层。[S031: config.json] |
| hidden size | text hidden size 4096；vision hidden size 1152。[S030: config.json] | text hidden size 2048；vision hidden size 1152。[S031: config.json] |
| attention mechanism | alternating `linear_attention`/`full_attention`，`full_attention_interval=4`；32 attention heads，2 KV heads，head dim 256。[S030: config.json] | alternating `linear_attention`/`full_attention`，`full_attention_interval=4`；16 attention heads，2 KV heads，head dim 256。[S031: config.json] |
| positional encoding | mRoPE 参数：`rope_theta=10000000`，`partial_rotary_factor=0.25`，`mrope_section=[11,11,10]`。[S030: config.json] | mRoPE 参数：`rope_theta=10000000`，`partial_rotary_factor=0.25`，`mrope_section=[11,11,10]`。[S031: config.json] |
| experts/router | 512 experts，10 experts/token，shared expert intermediate size 1024，router aux loss 0.001。[S030: config.json] | 256 experts，8 experts/token，shared expert intermediate size 512，router aux loss 0.001。[S031: config.json] |
| context window | `max_position_embeddings=262144`。[S030: config.json] | `max_position_embeddings=262144`。[S031: config.json] |
| tokenizer/vocab | `vocab_size=248320`。[S030: config.json] | `vocab_size=248320`。[S031: config.json] |
| modal encoder | vision depth 27，patch size 16，temporal patch size 2，spatial merge size 2，out hidden size 4096。[S030: config.json] | vision depth 27，patch size 16，temporal patch size 2，spatial merge size 2，out hidden size 2048。[S031: config.json] |
| output heads/modalities | image-text-to-text；文本输出。[S030: config.json] | image-text-to-text；文本输出。[S031: config.json] |
| reasoning/test-time structure | 官方未披露。[S030: config.json] | 官方未披露。[S031: config.json] |
| deployment formats | Hugging Face、ModelScope、推理平台。[S019: repository][S030: config.json] | Hugging Face、ModelScope、推理平台。[S019: repository][S031: config.json] |
| officially undisclosed | 完整训练数据、优化器、完整后训练配方、推理时 reasoning 内部结构。[S019: repository][S030: config.json] | 完整训练数据、优化器、完整后训练配方、推理时 reasoning 内部结构。[S019: repository][S031: config.json] |

## 推理/产品系统结构

Qwen 的 config 披露了模型结构本体；ModelScope/HF/推理平台属于部署渠道，不作为内部结构字段。[S019: repository][S030: config.json]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。Qwen 的 alternating attention 与 MoE 结构是官方结构事实，但 LMArena 分数仍是人类偏好结果。[S050: schema]

## 核心优势

Qwen3.5/3.6 的结构透明度很高：专家数、experts/token、linear/full attention 交替、mRoPE、vision tower 和 vocab 都有官方 config 字段。[S030: config.json][S031: config.json]

## 核心短板

训练 token 数、数据配比、优化器和后训练配方未完整披露；reasoning/test-time 内部结构未披露。[S019: repository][S030: config.json]

## 与其他模型的关键区别

Qwen 是本库中少数同时公开 MoE、vision tower、mRoPE 与 alternating linear/full attention 的开放权重模型；与 Mistral Large 3 相比结构字段更细。[S030: config.json][S031: config.json][S026: docs]

## 未公开信息

完整训练数据、优化器、训练基础设施、稳定性方法、完整后训练配方、reasoning/test-time 内部结构官方未披露。[S019: repository][S030: config.json][S031: config.json]

## claim-to-source map

- C018 -> S030
- C019 -> S031
