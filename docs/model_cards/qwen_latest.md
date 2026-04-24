# Qwen 最新模型卡

- 最新模型名称：Qwen3.6-35B-A3B；Qwen3.5-397B-A17B 是 2026 旗舰 family 之一。[S019: News]
- 发布时间：Qwen3.6-35B-A3B 2026-04-16；Qwen3.5 首发 2026-02-16。[S019: News]
- 开放程度：Hugging Face/ModelScope 发布；Qwen3 family 多数 Apache 2.0，具体逐模型以 model card 为准。[S019: Models]
- 架构：MoE/hybrid family；Qwen3.5-397B-A17B 从命名披露 397B total/17B active。[S019: Models]
- 预训练：完整数据规模和配比需官方 release blog/model card；本项目不猜测。
- 后训练：thinking/non-thinking lineage 和 tool/coding 能力需逐模型卡更新。
- 推理方式：长上下文、vLLM/SGLang/ModelScope/HF 支持，具体上下文按模型卡。[S019: Models]
- 微调/部署：开放权重，Hugging Face/ModelScope，本地与企业部署友好。[S019: Models]
- LMArena 最新表现：qwen3-vl-235b-a22b-instruct rank 74、rating 1415.9；qwen3.5-397b-a17b 在 2026-04-14 viewer snippet rank 36。[S051: rows][S050: viewer rows]
- 核心优势：开放生态完整、尺寸覆盖广、多语言与中文能力强。
- 核心短板：模型族复杂，必须逐模型核对 license/context/modalities。
- 与其他模型关键区别：Qwen 是“全尺寸开放模型族”，适合从端侧到集群多级部署。
- 未公开信息：Qwen3.6 完整训练细节、逐模型数据配比。
- claim-to-source map：S019。

