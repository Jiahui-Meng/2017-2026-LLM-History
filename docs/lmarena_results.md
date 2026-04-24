# LMArena Results

固定快照见 `data/lmarena_latest.csv`。本项目使用的主数据源是 Hugging Face `lmarena-ai/leaderboard-dataset`，其 subsets 包括 `text`, `text_style_control`, `vision`, `vision_style_control`, `search`, `search_style_control`, `document`, `document_style_control`, `webdev`, `text_to_image`, `image_edit` 等。[S050: Subsets]

## 观察

- `text_style_control/latest` 中 Claude Opus 4.7 thinking 位居前列，但早期票数较 Claude Opus 4.6 thinking 少，应关注置信区间和 vote_count。[S051: rows]
- WebDev/Code 榜单对 agentic coding、工具使用、前端审美和脚手架适配更敏感，Claude Opus thinking、GPT-5.2-high、Gemini 3 Pro、GLM-4.7、MiniMax-M2.1 均靠前。[S052: webdev latest]
- Text-to-Image 榜单主要评估图像生成模型，不应与文本 LLM Overall 直接合并排名；GPT Image 1.5 与 Gemini 3 Pro Image 是该类别前列。[S053: text_to_image latest]
- Vision 榜单显示 Gemini 3 Pro、Gemini 3 Flash、OpenAI 高 effort 变体靠前，但视觉榜与 OCR、document 子类会有不同排序。[S054: vision latest]

