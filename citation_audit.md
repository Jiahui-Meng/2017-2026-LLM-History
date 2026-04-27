# Citation Audit

审计日期：2026-04-27

## 范围

本次审计覆盖新的时间线主页、`docs/llm_timeline.md`、家族历史页、专题页、`docs/architecture_innovations.md`、`data/timeline.yaml`、`data/families.yaml`、`data/claims.yaml`、`data/models.yaml` 与新的时间线/架构表格和图表。

## 主要来源分层

| 来源层级 | 用途 | 示例 |
|---|---|---|
| 官方论文 / 官方研究页 | 支撑历史里程碑与方法创新 | Transformer、GPT-1、BERT、T5、FLAN、Constitutional AI。[S036][S037][S038][S039][S042][S045] |
| 官方模型发布 / 产品文档 | 支撑近年家族节点、上下文、工具、产品能力 | GPT-5.x、Claude 4.7、Gemini 3、Kimi K2.6、GLM-5.1。[S001][S005][S008][S017][S022] |
| 官方 GitHub / Hugging Face config | 支撑开放权重结构事实 | DeepSeek、Qwen、Kimi、MiniMax、GLM、Llama 4、Mistral Large 3。[S015][S027][S028][S029][S030][S031][S032][S033][S035] |
| 排行榜 / 数据集 | 仅用于附录和当前快照，不用于补全结构事实 | LMArena dataset 与各子榜单。[S050][S051][S052][S053][S054] |

## 历史叙事里的引用原则

1. 时间线节点优先使用一手来源，且每个关键节点至少有 1 条可核验来源。
2. 闭源模型未公开的参数、专家数、层数、训练 token 与完整后训练配方统一写“官方未披露”。
3. 产品系统节点与 base model 节点强制分开引用，例如 ChatGPT、Muse Spark、Claude Code 不能被当作底层结构来源。
4. 开放权重模型若 config/model card 没有直接给出 active params 或训练配方，也不能从社区二手资料补齐。

## 架构创新专题的特殊边界

- `dense` 与 `MoE` 的比较优先使用论文、model card 和 config 中能直接核验的结构事实；不从 benchmark 反推结构优劣。
- `attention` 结构只记录官方明确公开的 full/hybrid/MLA/DSA/LoRA-rank/KV-head 等字段，不把社区解读当作事实。
- `产品系统能力` 与 `base model architecture` 继续强制分离；例如 ChatGPT、Claude Code、Muse Spark 不能拿来证明底层 attention 或 dense/MoE 路线。

## 当前高风险项

- `ChatGPT` 作为 2022 产品节点，公开可核验材料更偏产品与对齐而非技术报告；因此时间线里把它记作 `product node`，不拿它证明 GPT-4/5 的内部结构。
- `Kimi` 早期长上下文阶段的公开英文材料分散，当前以官方平台文档与模型列表为主，不写未正式公开的传闻节点。[S017][S018][S061]
- `Meta` 必须拆成 `Llama` 与 `Muse Spark` 两条线；后者是产品系统，前者是基础模型家族。[S011][S033][S034]
- `DeepSeek-R1` 与 `DeepSeek-V3.2` 分别代表 reasoning RL 和 tool-use thinking，两者不能互相替代。[S014][S057]
- `Qwen3.x` 的 hybrid attention、`DeepSeek/GLM` 的 MLA/DSA、`Kimi` 的多模态结构字段都属于不同层级的架构创新，不能混写成单一“attention 更好”结论。[S027][S028][S030][S031][S032]

## 数据层检查

- `data/timeline.yaml` 中所有 source id 均已在 `data/sources.yaml` 注册。
- `data/claims.yaml` 的每条 claim 均包含 `improvement`、`innovation`、`impact` 三项历史叙事字段；本轮新增 C021-C023 覆盖 dense/MoE、hybrid attention 与 MLA/DSA。
- `docs/`、`tables/`、`README.md` 中引用的 source id 已核对，无缺失项。

## 后续维护建议

1. 新增模型时，先判断它是 `paper`、`model` 还是 `product` 节点，再写入时间线。
2. 若闭源公司发布新的 system card 或技术报告，优先补充“为何比前代强”和“哪些仍未披露”。
3. 若开源家族公开新的 config/model card，可补结构页，但不要倒推历史节点未公开字段。
