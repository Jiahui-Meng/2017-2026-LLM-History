# Citation Audit

审计日期：2026-04-24

## 范围

本次审计覆盖新增“模型结构”字段、`data/comparison_matrix.csv`、`docs/architecture_comparison.md`、`tables/architecture_comparison.md`、`docs/unknowns_and_confidence.md` 和 11 张模型卡。

## 结构来源

| source id | 用途 | 状态 |
|---|---|---|
| S001-S004 | OpenAI GPT-5.5/GPT-5.4 发布、系统卡、ChatGPT/Codex/API 可用性 | 已引用 |
| S005-S006 | Claude Opus 4.7 发布与产品信息 | 已引用 |
| S008-S010 | Gemini 3/3.1 Pro 模型表、开发者指南、发布信息 | 已引用 |
| S011 | Muse Spark / Meta AI 产品系统背景 | 已引用为产品系统，不写入 Llama base structure |
| S012, S033-S034 | Llama 4 Scout/Maverick model card 与 context/spec 信息 | 已引用 |
| S014-S016, S028 | DeepSeek-V3.2 发布、背景 repo、config.json | 已引用 |
| S017-S018, S027 | Kimi model list 与 Kimi K2.6 config.json | 已引用 |
| S019, S030-S031 | Qwen repo 与 Qwen3.5/Qwen3.6 config.json | 已引用 |
| S020-S021, S029 | MiniMax model card/post-training/config.json | 已引用 |
| S022-S023, S032 | GLM/Z.ai 文档与 GLM-5.1 config.json | 已引用 |
| S024 | xAI API model table | 已引用 |
| S025-S026, S035 | Mistral Large 3 announcement/docs/HF model card | 已引用 |
| S050-S054 | LMArena dataset/leaderboard 来源 | 已引用于 LMArena 方法与结果 |

## Claim-Level 覆盖

- C015-C020 覆盖 Kimi、DeepSeek、MiniMax、Qwen、GLM 的 config 级结构字段。
- C021-C022 覆盖 Llama 4 Maverick 与 Mistral Large 3 的官方 model card/docs 结构字段。
- C001-C014 保留模型发布时间、能力、接口与 LMArena 方法事实。

## 官方披露边界

- 闭源模型的参数、层数、hidden size、attention、experts/router、tokenizer/vocab 均标为“官方未披露”。
- 开放权重模型如果 config/model card 没有直接给 active params，也标为“官方未披露”，并仅记录 experts/token 等已公开 routing 字段。
- DeepSeek-V3 早期技术报告数字只作为背景，不填入 DeepSeek-V3.2 未披露字段。
- LMArena 不用于补全结构事实，也不作为绝对智能评测。

## 待复核项

1. 后续若 OpenAI、Anthropic、Google、xAI 发布系统卡或技术报告，优先补齐底层结构字段。
2. 若 Llama 4 gated repo 后续公开 config.json，应更新 layers、hidden size、attention、tokenizer/vocab 和 vision encoder 字段。
3. 若 Mistral Large 3 公开 config.json，应更新 experts/router、layers、hidden size、attention 与 tokenizer/vocab 字段。
4. 每次更新 LMArena 时记录 dataset、split、leaderboard_publish_date、vote_count、rating_lower/rating_upper 与 preliminary 状态。
