# Moonshot/Kimi 最新模型卡：Kimi K2.6

## 基本信息

- 最新公开模型：Kimi K2.6，官方模型列表将其列为推荐模型，支持原生多模态、256k context、thinking 与 non-thinking 模式。[S017: model list]
- 开放程度：开放权重 + Kimi API；HF config 公开了详细 text/vision 结构字段。[S017: model list][S027: config.json]

## 模型结构（官方披露）

| field | Kimi K2.6 官方结构信息 |
|---|---|
| architecture family | `KimiK25ForConditionalGeneration`；`text_config` 使用 `DeepseekV3ForCausalLM`/`kimi_k2`。[S027: config.json] |
| dense/MoE | MoE。[S027: config.json] |
| total params | HF metadata 约 1,058,589.4M。[S027: config.json] |
| active params | 官方未披露；config 公开 `num_experts_per_tok=8`，不等同于 active params。[S027: config.json] |
| layers | text 61 层；vision 27 层。[S027: config.json] |
| hidden size | text hidden size 7168；vision hidden size 1152；vision intermediate size 4304。[S027: config.json] |
| attention mechanism | text 64 attention heads、64 KV heads；`q_lora_rank=1536`、`kv_lora_rank=512`、`qk_nope_head_dim=128`、`qk_rope_head_dim=64`、`v_head_dim=128`。[S027: config.json] |
| positional encoding | YaRN RoPE scaling factor 64，`original_max_position_embeddings=4096`，`rope_theta=50000`。[S027: config.json] |
| experts/router | `n_routed_experts=384`，`n_shared_experts=1`，`num_experts_per_tok=8`，`moe_intermediate_size=2048`，`topk_method=noaux_tc`。[S027: config.json] |
| context window | `max_position_embeddings=262144`；官方模型列表写 256k context。[S017: model list][S027: config.json] |
| tokenizer/vocab | `vocab_size=163840`。[S027: config.json] |
| modal encoder | vision patch size 14；spatial-temporal video attention；patchmerger projector；vision 27 layers/16 heads。[S027: config.json] |
| output heads/modalities | image-text-to-text 任务；文本输出。[S027: config.json] |
| reasoning/test-time structure | 官方模型列表公开 thinking/non-thinking modes；内部 reasoning 结构官方未披露。[S017: model list] |
| deployment formats | Hugging Face、Kimi API、推理平台；config 另含 compressed-tensors int4 quantization 字段。[S017: model list][S027: config.json] |
| officially undisclosed | active params、完整训练数据、优化器、稳定性方法、完整后训练配方。[S017: model list][S027: config.json] |

## 推理/产品系统结构

thinking/non-thinking 是对外推理模式；Kimi API 的模型选择与产品工具结构不写入 base model 内部结构。[S017: model list]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。榜单偏好不能解释 Kimi K2.6 的 384 experts 或 vision tower 设计是否直接带来分数提升。[S050: schema]

## 核心优势

结构披露粒度高：超大 MoE、384 routed experts、长上下文、vision tower、YaRN RoPE 和 int4 部署字段都可从官方 config 审计。[S027: config.json]

## 核心短板

active params 与完整训练/后训练配方仍官方未披露；1T 级 total params 也意味着本地部署成本高。[S027: config.json]

## 与其他模型的关键区别

Kimi K2.6 公开了比 Mistral Large 3 更细的 config 结构，比闭源 GPT/Claude/Gemini/Grok 更透明；其 vision tower 结构也比 Llama 4 model card 更具体。[S027: config.json][S033: model card]

## 未公开信息

active params、训练 token 数、数据配比、优化器、训练基础设施、稳定性方法、完整 SFT/RL/安全后训练配方官方未披露。[S017: model list][S027: config.json]

## claim-to-source map

- C009 -> S017
- C015 -> S027
