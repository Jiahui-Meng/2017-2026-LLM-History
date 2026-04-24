# 架构结构表

| 模型 | dense/MoE | total / active params | layers | hidden size | attention | position | experts/router | context | tokenizer/vocab | modal encoder | deployment | citation |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| GPT-5.5 / GPT-5.4 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | GPT-5.4 1M | 官方未披露 | 图像输入能力；编码器未披露 | ChatGPT/Codex/API for GPT-5.4 | [S001][S002][S003] |
| Claude Opus 4.7 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 1M | 官方未披露 | 图像输入；编码器未披露 | Claude/API/Bedrock/Vertex/Microsoft Foundry | [S005][S006] |
| Gemini 3.1 Pro / 3 Pro | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 1,048,576 input / 65,536 output | 官方未披露 | 文本/图像/视频/音频/PDF；编码器未披露 | Gemini API/Vertex/Gemini app | [S008][S009][S010] |
| Llama 4 Maverick | MoE | 约 401.6B / 17B | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 128E；router 未披露 | 1M | 官方未披露 | 图像+文本；编码器未披露 | HF gated/open-weight | [S012][S033] |
| Llama 4 Scout | MoE | 109B / 17B | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 16E；router 未披露 | 10M | 官方未披露 | 图像+文本；编码器未披露 | HF gated/open-weight | [S012][S034] |
| Kimi K2.6 | MoE | 约 1,058,589.4M / active 官方未披露 | text 61; vision 27 | text 7168; vision 1152 | q_lora_rank 1536; kv_lora_rank 512; 64 heads | YaRN factor 64; rope_theta 50000 | 384 routed; 1 shared; 8/token | 262144 | 163840 | patch 14; spatial-temporal video attention; patchmerger | HF/API/int4 config | [S017][S027] |
| DeepSeek-V3.2 | MoE | 约 685,396.9M / active 官方未披露 | 61 | 7168 | q_lora_rank 1536; kv_lora_rank 512; DSA index heads 64/topk 2048 | YaRN factor 40; rope_theta 10000 | 256 routed; 1 shared; 8/token | 163840 | 129280 | 无 | HF/API/FP8 config | [S014][S028] |
| Qwen3.5-397B-A17B | MoE | 约 403,397.9M / A17B model name | text 60; vision 27 | text 4096; vision 1152 | alternating linear/full; 32 heads; 2 KV | mRoPE theta 10000000 | 512 experts; 10/token | 262144 | 248320 | patch 16; temporal patch 2 | HF/ModelScope | [S019][S030] |
| Qwen3.6-35B-A3B | MoE | 约 35,951.8M / A3B model name | text 40; vision 27 | text 2048; vision 1152 | alternating linear/full; 16 heads; 2 KV | mRoPE theta 10000000 | 256 experts; 8/token | 262144 | 248320 | patch 16; temporal patch 2 | HF/ModelScope | [S019][S031] |
| MiniMax-M2.1 | MoE | 约 228,703.6M / 10B | 62 | 3072 | 48 heads; 8 KV; qk_norm | RoPE theta 5000000 | 256 local; 8/token; routing bias | 196608 | 200064 | 无 | HF/API/SGLang/vLLM/Transformers | [S020][S029] |
| GLM-5.1 | MoE + DSA | 约 753,864.1M / active 官方未披露 | 78 | 6144 | DSA index heads 32/topk 2048; q_lora_rank 2048; kv_lora_rank 512 | RoPE theta 1000000 | 256 routed; 1 shared; 8/token | 202752 | 154880 | 无 | HF/Z.ai API/bf16 | [S022][S032] |
| Grok 4.20 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | 2M | 官方未披露 | image token pricing；编码器未披露 | xAI API | [S024] |
| Mistral Large 3 | Sparse MoE | 675B / 41B | 官方未披露 | 官方未披露 | 官方未披露 | 官方未披露 | granular sparse MoE；数量/router 未披露 | 256k | 官方未披露 | 图像理解；编码器未披露 | Apache 2.0 open-weight/API/cloud | [S025][S026][S035] |
