# MiniMax 最新模型卡：MiniMax-M2.1

## 基本信息

- 最新公开模型：MiniMax-M2.1，官方 model card 将其描述为约 230B total / 10B active 的 MoE 模型，面向 coding、tool use、instruction following 与 long-horizon planning。[S020: model card][S021: post-training]
- 开放程度：开放权重 + API；官方列出 SGLang、vLLM、Transformers、KTransformers、MLX-LM 等部署路径。[S020: model card]

## 模型结构（官方披露）

| field | MiniMax-M2.1 官方结构信息 |
|---|---|
| architecture family | `MiniMaxM2ForCausalLM`，`model_type=minimax_m2`。[S029: config.json] |
| dense/MoE | MoE。[S020: model card][S029: config.json] |
| total params | HF metadata 约 228,703.6M；model card 描述约 230B。[S020: model card][S029: config.json] |
| active params | model card 描述约 10B；config 公开 `num_experts_per_tok=8`。[S020: model card][S029: config.json] |
| layers | 62 层。[S029: config.json] |
| hidden size | hidden size 3072；intermediate size 1536。[S029: config.json] |
| attention mechanism | 48 attention heads，8 KV heads，head_dim 128，`use_qk_norm=true`，`qk_norm_type=per_layer`。[S029: config.json] |
| positional encoding | RoPE：`rope_theta=5000000`，`rotary_dim=64`。[S029: config.json] |
| experts/router | 256 local experts，8 experts/token，sigmoid scoring，routing bias enabled。[S029: config.json] |
| context window | `max_position_embeddings=196608`。[S029: config.json] |
| tokenizer/vocab | `vocab_size=200064`。[S029: config.json] |
| modal encoder | 无；M2.1 config 是文本模型结构。[S029: config.json] |
| output heads/modalities | 文本输出。[S029: config.json] |
| reasoning/test-time structure | config 含 MTP：`use_mtp=true`，3 MTP modules，1 MTP transformer layer；官方 post-training 文档描述 interleaved thinking。[S021: post-training][S029: config.json] |
| deployment formats | Hugging Face、API、SGLang、vLLM、Transformers、KTransformers、MLX-LM；config 含 FP8 quantization 字段。[S020: model card][S029: config.json] |
| officially undisclosed | 完整训练数据、优化器、训练基础设施、完整后训练配方。[S020: model card][S021: post-training] |

## 推理/产品系统结构

tool use、instruction following、interleaved thinking 和 long-horizon planning 是 MiniMax 的后训练/推理能力；config 中可审计的是 MoE、MTP、FP8 和长上下文字段。[S020: model card][S021: post-training][S029: config.json]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。榜单可记录用户偏好，但不能单独证明 MiniMax 的 MTP 或 MoE 是分数来源。[S050: schema]

## 核心优势

结构紧凑的高稀疏 MoE、10B active 公开描述、长上下文、MTP、FP8 与多推理后端支持。[S020: model card][S029: config.json]

## 核心短板

训练数据和完整 RL/后训练细节未全量公开；无官方多模态结构字段。[S020: model card][S021: post-training]

## 与其他模型的关键区别

MiniMax-M2.1 的 total/active 比例更偏高稀疏；相比 DeepSeek/Kimi，其 hidden size 更小但层数相近，并公开了 MTP module 数。[S027: config.json][S028: config.json][S029: config.json]

## 未公开信息

训练 token 数、数据配比、优化器、训练基础设施、稳定性方法、完整 SFT/RL/safety 配方官方未披露。[S020: model card][S021: post-training]

## claim-to-source map

- C010 -> S020, S021
- C017 -> S029
