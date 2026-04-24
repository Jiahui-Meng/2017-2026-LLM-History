# Z.ai/GLM 最新模型卡：GLM-5.1

## 基本信息

- 最新公开模型：GLM-5.1，官方文档将其定位为 long-horizon tasks、thinking、MCP/function calling 等能力的旗舰模型。[S022: overview]
- 开放程度：开放权重 + Z.ai API；HF config 公开 `GlmMoeDsaForCausalLM` 结构字段。[S022: overview][S032: config.json]

## 模型结构（官方披露）

| field | GLM-5.1 官方结构信息 |
|---|---|
| architecture family | `GlmMoeDsaForCausalLM`，`model_type=glm_moe_dsa`。[S032: config.json] |
| dense/MoE | MoE + DSA 字段。[S032: config.json] |
| total params | HF metadata 约 753,864.1M。[S032: config.json] |
| active params | 官方未披露；config 公开 `num_experts_per_tok=8`，不等同于 active params。[S032: config.json] |
| layers | 78 层。[S032: config.json] |
| hidden size | hidden size 6144；intermediate size 12288。[S032: config.json] |
| attention mechanism | DSA/index 字段：`index_n_heads=32`、`index_topk=2048`、`index_head_dim=128`；`q_lora_rank=2048`、`kv_lora_rank=512`、64 attention heads，64 KV heads，head_dim 64。[S032: config.json] |
| positional encoding | `rope_theta=1000000`，`rope_type=default`，`rope_interleave=true`，`indexer_rope_interleave=true`。[S032: config.json] |
| experts/router | `n_routed_experts=256`，`n_shared_experts=1`，`num_experts_per_tok=8`，`moe_intermediate_size=2048`，`topk_method=noaux_tc`。[S032: config.json] |
| context window | `max_position_embeddings=202752`；官方文档写 200K context 和 128K maximum output tokens。[S022: overview][S032: config.json] |
| tokenizer/vocab | `vocab_size=154880`。[S032: config.json] |
| modal encoder | 无；GLM-5.1 config 是文本模型结构。[S032: config.json] |
| output heads/modalities | 文本输出。[S032: config.json] |
| reasoning/test-time structure | 官方公开 thinking mode、long-horizon execution、MCP/function calling；内部 reasoning 结构官方未披露。[S022: overview] |
| deployment formats | Hugging Face、Z.ai API、推理平台；config dtype 为 bf16。[S022: overview][S032: config.json] |
| officially undisclosed | active params、完整训练数据、优化器、完整后训练配方、reasoning 内部结构。[S022: overview][S032: config.json] |

## 推理/产品系统结构

MCP、function calling 和 long-horizon execution 是平台/推理系统能力；模型结构表只记录 config 明确披露的 MoE/DSA/RoPE/context 字段。[S022: overview][S032: config.json]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。GLM 的 DSA/MoE 字段可审计，但 LMArena 不提供结构因果证据。[S050: schema]

## 核心优势

GLM-5.1 在官方 config 中公开 78 层、6144 hidden size、256 routed experts、DSA index heads、202752 max positions 与 154880 vocab。[S032: config.json]

## 核心短板

active params、训练数据、优化器和完整后训练配方官方未披露；多模态结构不在 GLM-5.1 config 中。[S022: overview][S032: config.json]

## 与其他模型的关键区别

GLM-5.1 与 DeepSeek-V3.2 都公开 DSA/index 字段；GLM 层数更多、hidden size 更小，context window 介于 DeepSeek-V3.2 与 Kimi/Qwen 之间。[S028: config.json][S032: config.json][S027: config.json][S030: config.json]

## 未公开信息

active params、训练 token 数、数据配比、优化器、训练基础设施、完整 SFT/RL/safety 后训练配方与 reasoning 内部结构官方未披露。[S022: overview][S032: config.json]

## claim-to-source map

- C011 -> S022
- C020 -> S032
