# Citation Audit

审计日期：2026-04-24。

## 覆盖情况

- 官方来源：OpenAI、Anthropic、Google、Meta、DeepSeek、Kimi、Qwen、MiniMax、Z.ai、xAI、Mistral 均有来源条目。[S001][S005][S009][S011][S014][S017][S019][S020][S022][S024][S025]
- LMArena：使用 Hugging Face `lmarena-ai/leaderboard-dataset` 作为主来源，并记录 schema、subsets、splits、methodology notes。[S050]
- Claim map：`data/claims.yaml` 记录 C001-C014，覆盖最新模型、架构、训练、推理、LMArena 方法论。

## 高风险结论

| 风险 | 处理 |
|---|---|
| 闭源模型参数规模 | 一律写“官方未披露”。 |
| 第三方架构推断 | 不进入主表事实列，只可在注释中标“第三方”。 |
| LMArena 快照变动 | CSV 记录 `leaderboard_publish_date`；README 明确检索日和榜单日分离。 |
| Low vote_count / preliminary | LMArena 章节要求同时看 CI 和 vote_count。 |
| Product capability vs base architecture | docs 中反复标注 tools/search/computer use 属于系统能力。 |

## 待补

- 用 dataset API 重抓 `document`, `document_style_control`, `search`, `search_style_control`, `image_edit` 的具体 top rows。
- 为 Kimi K2.6、Qwen3.6、GLM-5.1 补充官方 Hugging Face/GitHub model card 的完整参数与 license。
- 若 OpenAI GPT-5.5 API 发布，更新 OpenAI 模型卡和 comparison matrix。

