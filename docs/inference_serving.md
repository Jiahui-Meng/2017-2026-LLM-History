# 推理与部署

| 能力 | 代表 | 说明 |
|---|---|---|
| Thinking/reasoning effort | GPT-5.4、Claude Opus 4.7、Gemini 3、Kimi K2.6、GLM-5.1、Grok 4.20 | 推理预算成为 API/产品控制面。[S003: GPT-5.4][S005: xhigh][S009: Model table][S017: Model List][S022: Capability][S024: API table] |
| Long-context serving | GPT-5.4 1M、Claude Opus 4.7 1M、Gemini 3 1M、Grok 4.20 2M、Llama Scout 10M | 上下文长度不能直接等同可用推理质量，需结合任务和 KV/attention 成本测试。[S003: Computer use][S006: product page][S009: Model table][S024: API table][S013: Llama specs] |
| KV/attention 优化 | DeepSeek MLA/DSA、Llama iRoPE/NoPE、Mistral MoE kernels | 主要目标是降低长上下文与稀疏模型 serving 成本。[S015: Model Summary][S016: DSA][S012: iRoPE][S025: NVIDIA collaboration] |
| Quantization | Kimi INT4、Mistral NVFP4、Llama int4、MiniMax FP8/BF16 | 开放权重模型正把低比特部署作为发布卖点。[S018: K2 overview][S025: NVFP4][S013: Llama specs][S020: model card] |
| Tool calling/computer use/search | GPT-5.4、Gemini 3、Grok 4.20、GLM-5.1 | 多数属于 product/API system capability，不能直接写成架构能力。[S003: Tools][S009: Model table][S024: API table][S022: Capability] |

