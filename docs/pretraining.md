# 预训练

预训练公开程度呈明显分层：开放权重模型通常披露更多参数与训练路线；闭源模型多只披露能力与安全评估。[S015: Model Summary][S025: Mistral Large 3]

| 模型 | 数据规模/类型 | 基础设施 | 稳定性/优化 |
|---|---|---|---|
| GPT-5.5 | 官方未披露 | 官方未披露 | system card 披露预部署安全评估，非完整训练细节。[S002: Introduction] |
| GPT-5.4 | 官方未披露 | 官方未披露 | 强调比 GPT-5.2 更 token efficient。[S003: Intro] |
| Claude Opus 4.7 | 官方未披露 | 官方未披露 | 官方提到训练中尝试 differential reduction 降低高风险 cyber 能力。[S005: Safety] |
| Gemini 3 | 官方未披露 | 官方未披露 | 官方披露 knowledge cutoff 与 capability，不披露训练规模。[S009: Model table] |
| DeepSeek-V3 lineage | 14.8T tokens，多样高质量语料；V3 使用 FP8、稳定训练无不可恢复 loss spikes。[S015: Introduction] | 2.788M H800 GPU hours。[S015: Introduction] | auxiliary-loss-free load balancing、MTP。[S015: Model Summary] |
| Mistral Large 3 | 训练数据配比未披露 | 从零训练于 3000 NVIDIA H200 GPUs。[S025: Mistral Large 3] | NVIDIA/vLLM/Red Hat 优化 serving；非完整优化器说明。[S025: NVIDIA collaboration] |
| MiniMax-M2.1 | 官方未披露完整预训练数据 | 官方未披露 | M2.1 重点披露后训练而非预训练。[S021: Model Overview] |

