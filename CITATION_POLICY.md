# Citation Policy

本项目采用 claim-level citation。每个关键事实必须在句末或表格单元格内放置来源，例如：

- DeepSeek-V3.2 是 V3.2-Exp 的正式继任者，并引入 reasoning-first 与 thinking in tool-use。[S014: Release]
- GPT-5.5 暂未在 API 发布，ChatGPT/Codex 分阶段推出。[S004: ChatGPT rollout]
- LMArena `text_style_control/latest` 使用 `rank/rating/rating_lower/rating_upper/vote_count/category/model_name/leaderboard_publish_date` 字段。[S050: Schema]

## 来源优先级

| 等级 | 来源类型 | 用途 |
|---|---|---|
| A | 官方模型页、官方博客、官方 API 文档、官方 model card | 模型名称、发布时间、上下文、接口能力、许可、官方 benchmark |
| B | 官方 GitHub/Hugging Face repo | 开放权重、参数、license、部署和推理格式 |
| C | LMArena/Hugging Face leaderboard dataset | 人类偏好榜单数据 |
| D | 第三方媒体/博客 | 仅作背景或“第三方称”，不可用于闭源架构定论 |

## 禁止写法

- 禁止把闭源模型参数写成估计值。
- 禁止只引用 LMArena Overall rank 推断“模型绝对更聪明”。
- 禁止把 product system 能力写成 base model 架构能力，除非官方明确说明。
- 禁止把 low vote_count/preliminary 榜单结果写成稳定结论。

