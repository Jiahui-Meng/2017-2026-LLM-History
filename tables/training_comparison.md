# Training Comparison

| 模型 | 预训练披露 | 训练基础设施 | 稳定性/优化 |
|---|---|---|---|
| DeepSeek-V3 lineage | 14.8T tokens。[S015: Introduction] | 2.788M H800 GPU hours。[S015: Introduction] | no irrecoverable loss spikes/rollbacks。[S015: Introduction] |
| Mistral Large 3 | 数据配比未披露 | 3000 NVIDIA H200 GPUs。[S025: Mistral Large 3] | serving 优化披露较多。[S025: NVIDIA collaboration] |
| GPT-5.5 | 官方未披露 | 官方未披露 | 安全评估披露。[S002: Introduction] |
| Claude Opus 4.7 | 官方未披露 | 官方未披露 | cyber differential reduction 公开提及。[S005: Safety] |
| Gemini 3 | 官方未披露 | 官方未披露 | knowledge cutoff Jan 2025。[S009: Model table] |

