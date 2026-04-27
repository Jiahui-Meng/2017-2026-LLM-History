# Architecture Innovation Matrix

| 结构维度 | 代表节点 | 关键区别 | 为什么重要 |
|---|---|---|---|
| Dense Transformer | Transformer / GPT-1 / GPT-3 / T5 | 所有 token 激活同一套主要参数 | 结构简单、训练稳定，但扩总容量成本高。[S036][S037][S039][S040] |
| Sparse MoE | Mixtral / DeepSeek-V3.2 / Qwen3.x / Llama 4 / Mistral Large 3 | 每个 token 只激活少量专家 | 用更低 active cost 换更大总容量。[S056][S028][S030][S031][S033][S035] |
| Router 设计 | DeepSeek-V3.2 / Kimi K2.6 / MiniMax-M2.1 / GLM-5.1 | routed experts、shared expert、experts/token、routing bias 各不相同 | 同样叫 MoE，但路由策略和成本结构并不相同。[S027][S028][S029][S032] |
| Hybrid Attention | Qwen3.5 / Qwen3.6 | alternating linear attention 与 full attention | 说明 attention 已按层分化，不再统一。[S030][S031] |
| MLA / DSA | DeepSeek-V3.2 / GLM-5.1 | attention/KV 路径有额外效率结构字段 | 目标是长上下文和推理效率，而不是只换专家数。[S028][S032] |
| KV / head design | MiniMax-M2.1 / Qwen3.x / Kimi K2.6 | KV heads、qk_norm、LoRA-rank 等字段不同 | 影响推理吞吐、缓存成本和稳定性。[S027][S029][S030][S031] |
| Position / RoPE variants | DeepSeek-V3.2 / Kimi K2.6 / Qwen3.x / GLM-5.1 / MiniMax-M2.1 | YaRN、mRoPE、不同 rope_theta | 长上下文不只是数字，更是位置编码工程。[S027][S028][S029][S030][S031][S032] |
| Multimodal structure | Kimi K2.6 / Qwen3.x / Llama 4 | 公开 vision config 或 image-text-to-text 路线 | 多模态已进入模型骨架，而不是纯产品外壳。[S027][S030][S031][S033][S034] |
