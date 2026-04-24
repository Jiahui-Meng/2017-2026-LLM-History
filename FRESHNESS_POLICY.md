# Freshness Policy

更新时间基准：2026-04-24，时区 Asia/Hong_Kong。

1. “最新模型”必须以检索日可访问的官方来源为优先：官方模型页、官方博客、官方 API 文档、官方 Hugging Face/GitHub model card。[S001: Intro][S005: Intro][S008: Models][S017: Model List]
2. 如果官方资料和 LMArena 出现模型名差异，以官方资料描述“公开可用状态”，以 LMArena 描述“榜单出现状态”；二者不得互相替代。[S050: Schema]
3. LMArena 必须记录 `leaderboard_publish_date`，不得把抓取日期当作榜单日期。[S050: Schema]
4. 榜单数据以 `latest` split 为当前快照；若 API 或 Hugging Face viewer 返回不同日期，保留文件中的快照日期并在注释中说明。[S050: Splits]
5. 闭源模型的参数规模、专家数、训练 token、训练硬件、优化器若官方未披露，一律写“官方未披露”；不得用媒体估计补表。[S001: Intro][S005: Intro][S009: Meet Gemini 3][S024: API table]
6. 第三方资料仅可用于标注“第三方推断/第三方评测”，不能升级为官方事实。
7. 每次更新必须同步：`data/sources.yaml`、`data/claims.yaml`、`data/lmarena_latest.csv`、`citation_audit.md`。

