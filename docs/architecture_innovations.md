# 模型架构创新专题

这页专门回答一个问题：LLM 到底在“模型结构”上进化了什么。最重要的不是某家参数更大，而是 4 个维度的持续分化：`dense vs MoE`、`attention 结构`、`位置编码/长上下文`、`多模态结构`。

## 1. Dense 到 MoE

### Dense 路线

- 早期 GPT-1、GPT-3、BERT、T5 代表的主流 Transformer 路线，本质上都可以看作 dense：每个 token 在前向时都会经过同一套主要参数块。[S036][S037][S038][S039][S040]
- 这种路线的优点是训练和实现相对直接，行为也更容易统一；缺点是想继续扩大总容量时，推理成本会同步膨胀。

### Sparse MoE 路线

- Mixtral 把 sparse MoE 推成开源主流节点：总参数可以很大，但每个 token 只激活少量专家。[S056]
- 之后 DeepSeek、Qwen3.x、Kimi K2.6、MiniMax-M2.1、GLM-5.1、Llama 4、Mistral Large 3 都公开走向 MoE，但路线并不相同。[S028][S030][S031][S027][S029][S032][S033][S035]

### 各家 MoE 差异

- `Mixtral / Mistral`：把 sparse MoE 做成高效开源路线，强调容量与部署平衡。[S056][S025][S026]
- `DeepSeek`：MoE 之外还叠加 MLA、DSA、MTP，目标是同时优化容量、长上下文和推理效率。[S015][S028]
- `Qwen3.x`：MoE 和 hybrid attention 一起出现，不只是换成专家模型，而是在 attention 路径上也做结构变化。[S030][S031]
- `Kimi K2.6`：MoE 和原生多模态一起组织，文本与视觉结构同时公开。[S027]
- `MiniMax-M2.1`：更强调低 active params 和 agent/coding 任务效率。[S020][S029]
- `GLM-5.1`：把 MoE 和 DSA 结合，重点服务 long-horizon engineering tasks。[S022][S032]
- `Llama 4`：把 open-weight 多模态路线推进到 MoE 时代，但完整层级结构仍未完全公开。[S033][S034]

## 2. Attention 结构如何分化

### 标准 full self-attention

- Transformer 的出发点是标准 self-attention，它解决的是“所有 token 可以直接相互看见”的建模问题。[S036]
- GPT-1、GPT-3、BERT、T5 这类早期节点的历史意义主要在这里：先建立统一 attention 底座，再谈规模与后训练。[S037][S038][S039][S040]

### Hybrid / sparse / efficiency-oriented attention

- `Qwen3.5 / 3.6` 明确公开 alternating `linear_attention` 与 `full_attention`，说明 attention 已不再是“每层都一样”的默认设计。[S030][S031]
- `DeepSeek-V3.2` 与 `GLM-5.1` 则公开了 DSA/index 相关字段，以及 `q_lora_rank`、`kv_lora_rank` 这类效率导向结构参数。[S028][S032]
- `MiniMax-M2.1` 没有走同样的公开路径，但给出了 `qk_norm`、KV heads 和 RoPE 参数，说明它在 attention 稳定性和部署效率上有不同取舍。[S029]

### 关键结论

1. 2026 年的前沿开源模型已经不是“都在用同一种 Transformer”。
2. attention 结构的差异，越来越直接服务于长上下文、KV cache 成本、推理吞吐和部署效率，而不只是论文新奇度。

## 3. 位置编码与长上下文

- `RoPE` 及其变体已经成为多数前沿家族的基础做法，但具体实现差异很大。
- `Qwen3.x` 公开 `mRoPE` 参数。[S030][S031]
- `DeepSeek-V3.2` 与 `Kimi K2.6` 公开 `YaRN` scaling 与不同的 `rope_theta`。[S027][S028]
- `GLM-5.1` 与 `MiniMax-M2.1` 则给出各自的 RoPE 参数配置。[S029][S032]

这意味着“1M context”或“256K context”不是唯一重点，真正重要的是模型如何在结构层面把长上下文做得可训练、可推理、可部署。

## 4. 多模态结构

- `Qwen3.x` 和 `Kimi K2.6` 都在 config 里直接给出 vision 相关结构字段，说明多模态已经写进模型骨架，而不是外挂模块。[S027][S030][S031]
- `Llama 4` 明确是 image-text-to-text 路线，但 vision encoder 细节仍不完整公开。[S033][S034]
- `Gemini`、`GPT`、`Claude`、`Muse Spark` 则更多只公开输入输出能力和产品体验，内部视觉结构依旧未披露。[S005][S008][S011][S044]

## 5. 怎么读这些创新

不要把所有创新混成一个词。

- `dense vs MoE` 回答的是“参数如何被激活”。
- `attention 结构` 回答的是“token 之间如何交互、KV 成本如何控制”。
- `position / long-context` 回答的是“上下文如何被延展且仍然可用”。
- `multimodal structure` 回答的是“图像/视频/PDF 等模态是否真正写进模型骨架”。

真正强的模型，往往是在这几层同时有取舍，而不是只有一个亮点名词。
