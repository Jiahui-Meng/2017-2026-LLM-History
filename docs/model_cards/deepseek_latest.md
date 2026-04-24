# DeepSeek 最新模型卡：DeepSeek-V3.2

## 基本信息

- 最新公开模型：DeepSeek-V3.2，与 V3.2-Speciale 同期发布；官方说明 V3.2 支持 thinking in tool-use。[S014: release]
- 开放程度：开放权重 + API/应用渠道；HF config 公开详细结构字段。[S014: release][S028: config.json]

## 模型结构（官方披露）

| field | DeepSeek-V3.2 官方结构信息 |
|---|---|
| architecture family | `DeepseekV32ForCausalLM`，`model_type=deepseek_v32`。[S028: config.json] |
| dense/MoE | MoE。[S028: config.json] |
| total params | HF metadata 约 685,396.9M。[S028: config.json] |
| active params | V3.2 config 未直接披露；config 公开 `num_experts_per_tok=8`，不等同于 active params。[S028: config.json] |
| layers | 61 层。[S028: config.json] |
| hidden size | hidden size 7168；intermediate size 18432。[S028: config.json] |
| attention mechanism | MLA/DSA 风格字段：`q_lora_rank=1536`、`kv_lora_rank=512`、`qk_nope_head_dim=128`、`qk_rope_head_dim=64`、`v_head_dim=128`；128 attention heads / 128 KV heads；DSA index heads 64、index topk 2048。[S028: config.json] |
| positional encoding | YaRN RoPE scaling factor 40，`original_max_position_embeddings=4096`，`rope_theta=10000`。[S028: config.json] |
| experts/router | `n_routed_experts=256`，`n_shared_experts=1`，`num_experts_per_tok=8`，`first_k_dense_replace=3`，`topk_method=noaux_tc`，`topk_group=4`。[S028: config.json] |
| context window | `max_position_embeddings=163840`。[S028: config.json] |
| tokenizer/vocab | `vocab_size=129280`。[S028: config.json] |
| modal encoder | 无；V3.2 config 是文本模型结构。[S028: config.json] |
| output heads/modalities | 文本输出。[S028: config.json] |
| reasoning/test-time structure | V3.2 支持 thinking in tool-use；config 含 `num_nextn_predict_layers=1` 的 MTP 字段。[S014: release][S028: config.json] |
| deployment formats | Hugging Face、DeepSeek API、应用/网页渠道；config 含 FP8 quantization 字段。[S014: release][S028: config.json] |
| officially undisclosed | V3.2 active params、完整训练数据差异、优化器、完整后训练配方。[S014: release][S028: config.json] |

## 推理/产品系统结构

thinking in tool-use 是 DeepSeek-V3.2 的公开推理/工具使用能力；V3.2-Speciale 官方用于评测时不支持工具调用，这应与 base model 结构分开记录。[S014: release]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。DeepSeek 的 MoE/MLA/DSA 结构可审计，但 LMArena 仍只能表示人类偏好结果。[S050: schema]

## 核心优势

官方 config 披露 MoE、MLA/DSA 风格字段、YaRN RoPE、MTP、FP8 quantization 和 163840 context，结构透明度高。[S028: config.json]

## 核心短板

最新 V3.2 active params 与训练/后训练细节仍未在 config 或发布页完整披露；早期 V3 技术报告数字只作为背景，不填入 V3.2 未披露字段。[S014: release][S015: repository][S028: config.json]

## 与其他模型的关键区别

DeepSeek-V3.2 与 GLM-5.1 都公开 DSA/index 字段；与 Kimi K2.6 相比专家数更少、context window 更短；与闭源模型相比结构字段更完整。[S027: config.json][S028: config.json][S032: config.json]

## 未公开信息

V3.2 active params、训练 token 数、数据配比、优化器、训练基础设施、完整 SFT/RL/安全后训练配方官方未披露。[S014: release][S028: config.json]

## claim-to-source map

- C007 -> S014
- C016 -> S028
- C008 -> S015，仅作为早期 V3 背景
