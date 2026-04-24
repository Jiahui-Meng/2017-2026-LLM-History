# Architecture Comparison

见 `data/comparison_matrix.csv`。摘要：

| 模型 | 架构 | 参数 | context | 引用 |
|---|---|---|---|---|
| Llama 4 Maverick | MoE multimodal | 400B total / 17B active | 1M | [S013: Llama specs] |
| DeepSeek-V3 lineage | MoE + MLA | 671B / 37B active | 未在 V3.2 release 摘录中统一披露 | [S015: Introduction] |
| MiniMax-M2.1 | MoE | ~230B / ~10B active | 官方摘录未披露 | [S020: Overview] |
| Mistral Large 3 | Sparse MoE | 675B / 41B active | 256k | [S025: Mistral Large 3][S026: docs] |
| GPT/Claude/Gemini/Grok | 官方未披露 | 官方未披露 | 1M/2M 等接口 context | [S003: Computer use][S006: product page][S009: Model table][S024: API table] |

