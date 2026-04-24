# LMArena 方法论

LMArena/Arena Leaderboard 是人类偏好评测：用户在盲测中比较两个模型输出，榜单通过统计模型估计偏好强弱；它不是“绝对智能”测试，也不能替代安全、事实性、鲁棒性、成本、延迟、上下文稳定性或企业合规评估。[S050: dataset card]

## 必读字段

| 字段 | 解读 |
|---|---|
| `rank` | 当前 split/category 内排序，不应跨类别直接比较。[S050: Schema] |
| `rating` | Arena score；2024-01-09 后使用 Bradley-Terry 系统。[S050: Notes] |
| `rating_lower` / `rating_upper` | 置信区间边界；区间重叠时不要过度解读名次差。[S050: Schema] |
| `vote_count` | battle 数；票数低的 preliminary 模型不稳定。[S050: Schema] |
| `category` | overall/coding/math/vision 子类等，不同 category 测的是不同偏好。[S050: Schema] |
| `leaderboard_publish_date` | 榜单发布日期，必须和检索日期分开。[S050: Schema] |

Style Control 在 2025-05-16 成为 text/vision 默认，并调整 offset；因此 text_style_control 和旧 text 的时间序列不可无脑拼接。[S050: Notes]

