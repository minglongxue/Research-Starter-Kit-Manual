本文覆盖论文写作全链：整体策略，以及 Abstract、Introduction、Related Works、Methods、Experiments、Reference 各节的写法与常见错误。

## 08 · 如何写论文？（总览）

### 写论文之前

- **确定论文署名**：按贡献大小排序，主要写作由第一作者执笔，通讯作者是整个研究工作的负责人。
- **确定投稿目标**：根据工作水准挑选合适的发表源，一般由导师确定。

### 论文要说的其实就是这些

- Problem X is important
- Previous works A, B, and C have been done
- A, B, and C have their weakness
- Your Work D
- Why D is better
- Experimental comparison against A, B, and C
- Strength and Weakness of D
- Future work on D

### 论文大纲

科学论文有比较清晰的结构：Title → Abstract → Introduction → Related Works → Your Contribution（Method、Observation、Benchmark、Analysis 等）→ Support（Theoretical or Experimental）→ Conclusion。

> 图 8-1　论文的标准结构（ 示意图 ，据原文「论文大纲」绘制）　图示要点：Title / Abstract　（贡献说明书，五句话） / Introduction　（领域 → 已有工作 → 未解决 → 本文） / Related Works　（分类对比，为 gap 铺垫） / Your Contribution　（Method / Observation / Benchmark / Analysis） / Support　（理论推导 or 实验验证） / Conclusion

---

## 10 · 如何写论文 — Abstract

### 10.1　基本思路

论文摘要并非「论文简介」，而更应被视为一份**贡献说明书（statement of contribution）**。其目标不是全面概述论文内容，而是在有限篇幅内，使审稿人清晰地理解：本文解决了什么问题、提出了什么关键思想、以及这些贡献对领域的意义何在。因此，摘要不宜冗长，而应高度凝练、逻辑清晰。

### 10.2　五句话原则

在一般情况下，摘要可以遵循下面的「五句话原则」，对应五个核心要素：

> 图 10-1　Abstract 五句话原则的要素分配（ 示意图 ，据原文「五句话原则」绘制）　图示要点：任务背景 | 1 句：大方向 + 任务范畴，别铺垫常识 / 1–2 句：挑战与痛点要「结构性」 / 科学问题 / 「LLMs often fail in xxx」是经验现象 → 掉到 borderline；要上升到机理 / 最关键 / 方法创新 | 1–2 句：凝练思想，说清「为什么逻辑上能解决」 / 结论贡献 | 1 句：可量化（几个数据集、对比谁、提升多少） / 闭环检查：实验结论必须回扣前面提出的科学问题（说稳健性差，就用稳健性实验证明）

1. **任务背景（Context）— 1 句**：用最精炼的语言描述论文的大方向与任务范畴，使审稿人能够在第一时间判断论文所属领域以及所关注的核心问题。不要铺垫过多常识，直接切入主题。
2. **科学问题（Problem）— 1–2 句（最关键）**：这是比方法还要关键的部分，要讲出现有研究的挑战与痛点。理想情况下，这里要是一个「结构性问题」而不是一个「经验现象」，或者从经验现象出发总结出来的结构性问题。比如「LLMs often fail in xxxx task」就属于经验现象，给人一种修修补补、贡献不大的感觉，一下子就掉到了 borderline 区域；要给出更加本质的问题，从现象上升到机理——是理论有缺陷、泛化能力弱，还是稳健性不足？
3. **方法创新（Methodology）— 1–2 句**：提出核心的解决方案，尽可能凝练出思想，不要堆太多细节。比如要解决稳健性弱的问题，是通过什么方法解决的？提出了新的架构、新的损失，还是新的数据合成方法？核心思想是什么？关键在于让审稿人理解「为什么这种方法在逻辑上能够解决前述问题」。
4. **结论与贡献（Results）— 1 句**：实验描述应以具体、可量化的指标为主，而非泛泛而谈。很多同学喜欢直接写一句 significant performance improvement，这种写法很普通，因为所有论文都可以这么写；反之，明确指出在多少个数据集、对比了哪些代表性方法、在什么指标上取得了多大幅度的提升，会更具说服力。另外有一点非常重要但经常被忽略：**实验结论应当与前文提出的科学问题形成明确呼应与逻辑闭环**——如果论文声称解决的是稳健性不足的问题，实验中就应突出在何种干扰或变化下本文方法相较现有方法提升了多少稳健性；相比之下，仅报告整体 accuracy 往往不足以支撑核心 claim。

### 10.3　优秀案例

下面三个例子都来自 ICML 2025，分别对应「问题驱动型」「解决具体约束型」「Benchmark 型」三种最常见的摘要写法。

#### 案例 1 · 从问题分析出发提出算法

ICML 2025 Outstanding Paper：*Train for the Worst, Plan for the Best: Understanding Token Ordering in Masked Diffusions*

这是一篇从问题分析出发提出算法的文章。问题部分非常明确和本质：「trade off complexity at training time with flexibility at inference time」；结论部分极有说服力：**from 7% to 90%**，超越了 7 倍参数量的模型。

#### 案例 2 · 解决现有方法的某个具体约束

ICML 2025 Oral：*Accelerating LLM Inference with Lossless Speculative Decoding Algorithms for Heterogeneous Vocabularies*

非常常见的「解决现有 xxx 方法 xx 问题」的类型，跟大部分同学做的比较像。一句话确定背景：LLM 推理加速很重要；两句话指出问题：SD 方法 require the drafter and target models share the same vocabulary；一句话讲清本文工作：提出不依赖 shared-vocabulary constraint 的方法；实验回应 LLM 加速问题——不依赖约束，实现了 **2.8 倍加速**。

#### 案例 3 · Benchmark / 数据集类论文

ICML 2025 Oral：*LLM-SRBench: A New Benchmark for Scientific Equation Discovery with Large Language Models*

一句话确定背景：Scientific equation discovery 很重要；两句话明确背景与问题：LLM 用于 SR 得到了很多关注，但难以评估、不能反映真实能力；本文提出 LLM-SRBench，覆盖 239 个问题、4 个领域、2 大类别（LLM-Transform 与 LSR-Synth）；最后说明评估了多少模型——这里如果把 several SOTA methods 换成「评估了几类算法、多少个模型」会更好；结论点明发现了什么现象、对该领域有何贡献。

---

## 11 · 如何写论文 — Introduction

> **提示**　在了解完如何写Abstract之后，Introduction基本上是Abstract的扩写版本，依然是遵循以下的逻辑：
>
> 研究领域 → 已有工作 → 未解决问题 → 本文工作
> 一个好的Introduction，通常需要完成四件事情：
> - 说明研究领域为什么重要
> - 总结已有研究已经做了什么
> - 指出仍然存在的问题、空缺或不足
> - 说明本文要做什么，怎么做的，取得了什么样的结果

### 11.1　Introduction 的四段式结构

> 图 11-1　Introduction 的漏斗式四段结构（ 示意图 ，据原文「四段式结构」绘制）　图示要点：① 研究领域：为什么重要（科学 / 工程 / 产业价值） / ② 已有研究：别人做到了哪一步（分类 + 代表性工作） / ③ 未解决问题：现存缺口（gap） / ④ 本文工作：做了什么、怎么做的、结果如何

#### 1. 建立研究领域

第一部分要回答：这个领域为什么值得关注？

可以写：

- 该问题在科学、工程、医学、社会或产业中的重要性。
- 该方向近年来受到关注的原因。
- 该任务的应用场景或理论意义。
- 基本概念、对象或现象的简要定义。

注意：不要一上来就写自己的方法。先让读者理解这个问题为什么重要。

常见句式功能：

```
X is important because ...
X has received increasing attention due to ...
X plays a central role in ...
Recent advances in Y have made it possible to ...
```

#### 2. 回顾已有研究

第二部分要回答：别人已经做了什么？

这里不是写完整文献综述，而是选择与本文最相关的工作，为后面的 gap 做铺垫。

可以写：

- 已有方法的主要类别。
- 代表性工作解决了哪些问题。
- 这些工作带来了什么进展。
- 当前主流范式是什么。

常见句式功能：

```
Previous studies have investigated ...
Several methods have been proposed to ...
Existing approaches typically rely on ...
Recent work has shown that ...
```

#### 3. 指出问题或研究空缺

第三部分是 Introduction 的关键。它要回答：既然已有研究这么多，为什么还需要这篇论文？

可以指出：

- 现有方法仍然不能解决某类场景。
- 已有 benchmark无法准确评估某种能力。
- 现有数据、模型或理论存在限制。
- 过去工作忽略了某个重要变量。
- 现有结论尚不一致。
- 某个问题仍缺乏系统研究。
- ……

这一段要写得具体，不能只说 “However, this problem remains challenging.” 要说明到底 challenging 在哪里。

更好的写法是：

- 哪类场景下失败？
- 哪个假设不成立？
- 哪个能力没有被测到？
- 哪种成本过高？
- 哪类数据缺失？
- 哪个机制尚不清楚？

常见句式功能：

```
However, little is known about ...
Nevertheless, existing methods still suffer from ...
Despite these advances, ... remains unclear.
A key limitation of current approaches is ...
To date, few studies have systematically examined ...
```

#### 4. 引出本文工作

第四部分要回答：本文具体做了什么？

通常包括：

- 本文目标。
- 本文方法或研究对象。
- 本文主要贡献。
- 本文与已有工作的区别。
- 如有必要，简要说明论文结构。

注意：这一部分要清楚、直接，不要再继续铺垫。

可以写：

```
In this paper, we propose ...
Here, we investigate ...
We introduce a new benchmark for ...
Our approach differs from previous work in ...
The main contributions of this work are ...
```

### 11.2　段落组织建议

做到一段只讲一个核心观点，每段的开头第一句话（Topic Sentence）必须是“主题句”，告诉读者这段要讲什么，后面的句子围绕主题句展开（讨论、举例、描述）

一篇常规 Introduction 可以按 4-6 段组织：

#### 第 1 段：大背景

说明研究领域的重要性和基本问题。

#### 第 2 段：已有工作

总结已有方法、数据、理论或系统。

#### 第 3 段：不足与 gap

指出已有工作的限制，并把问题收窄到本文关注点。

#### 第 4 段：本文方法

说明本文提出什么方法、系统、数据集、benchmark 或理论分析。

#### 第 5 段：贡献总结

列出 2-4 条贡献。每条贡献应具体、可验证。

#### 第 6 段：论文结构

可选。部分期刊或长论文需要说明后文安排，机器学习会议论文通常可以省略。

### 11.3　一个可复用的写作骨架

**第 1 段：**

近年来，……问题在……领域中变得越来越重要。该问题的核心在于……，它对于……具有重要意义。

**第 2 段：**

已有研究主要从……角度解决该问题。例如，……方法关注……，……方法进一步……。这些工作推动了……的发展。

**第 3 段：**

然而，现有研究仍存在一个关键限制：……。具体而言，……。因此，在……场景下，已有方法难以……。

**第 4 段：**

为了解决这一问题，本文提出……。我们设计/构建/分析……，并通过……验证其有效性。

**第 5 段：**

本文的主要贡献包括：第一，……；第二，……；第三，……。

---

## 12 · 如何写论文 — Related Works

> **说明**　原手册该章为在线交互式页面，正文未能完整抓取。以下要点整理自手册其他章节的判据与常见审稿意见，供写作时参照。

Related Works 不是文献综述，它的唯一功能是**为本文的 gap 铺垫**：读完这一节，审稿人应当相信「这个问题确实还没被解决」。

四段结构：

1. **分类**：按方法范式（而非按时间或按作者）划分 2–4 类，每类给一个名字。
2. **代表工作**：每类挑 2–4 篇最有代表性的，一句话讲清其核心做法。
3. **局限**：每类结尾必须落到「这一类解决不了什么」，用同一把尺子衡量，便于横向对比。
4. **定位**：最后一段说明本文与上述各类的差异——本文属于哪一类、又突破了哪一点。

三条硬判据：

- **分类维度要正交**：不能出现「基于 CNN 的方法」与「基于注意力机制的方法」并列却互有交叠。
- **只夸不批等于没写**：每条引用后面必须有评价，且评价要指向本文要填的缺口。
- **与 Introduction 有分工**：Introduction 只提 3–5 篇最能建立动机的工作，Related Works 才展开完整对比；两处不要逐字重复。

常见翻车点：

- 流水账：「A 提出了…B 提出了…C 提出了…」，读者读完不知道谁更强、缺什么。
- 漏掉审稿人自己的论文，或漏掉最直接竞争的工作——这是被拒的高频理由。
- 把本文方法当成「某一类的一个实例」来介绍，等于自己放弃了 novelty 的表述权。

---

## 13 · 如何写论文 — Methods

> **提示**　Methods 应当是论文中相对最好写的部分，因为它主要回答一个问题：
>
> 本文的方法到底是怎么做的？
> 对于 AI 论文而言，Methods 通常需要把以下内容讲清楚：
> - 方法的核心思想。
> - 问题定义和符号系统。
> - 模型结构或算法流程。
> - 关键模块的设计动机。
> - 公式、目标函数、推导过程。

### 13.1　推荐采用“总分结构”

> 图 13-1　Methods 的总分结构（ 示意图 ，据原文「推荐采用总分结构」绘制）　图示要点：Overview：核心思想 + 模块分工 + 输入到输出的流程 / Problem | Method | Training / | Inference / / Formulation | Details | Optimization | Deployment / ↑ 从粗到细：先让人看懂「整体在做什么」，再讲「每个模块为什么这么设计」 / 主图负责「看见方法」，Overview 负责「理解这张图」——两者必须配套

Methods 一般适合采用总分结构：

- Overview：先总体介绍方法。
- Problem Formulation：定义问题和符号。
- Method Details：分模块讲方法。
- Training / Optimization：讲训练目标和优化方式。
- Inference / Deployment：讲测试或使用阶段如何运行。

这种结构的好处是，读者先看到方法全貌，再逐步进入细节，不会一开始就被公式、符号和模块名称淹没。

### 13.2　先写 Overview

Methods 开头通常应先写一段 Overview，用来介绍方法的核心思想。

Overview 不需要写太多细节，而是要回答：

- 本文方法要解决什么问题？
- 方法的基本出发点是什么？
- 方法由哪些主要模块组成？
- 每个模块大致负责什么？
- 整体流程如何从输入走到输出？

Overview 应该和方法的主图配合使用，主图负责让读者“看见方法”，Overview 负责让读者“理解这张图”。

### 13.3　单独写 Problem Formulation

AI 论文通常会出现很多字母、符号、变量、集合、函数和下标。如果不提前定义清楚，读者后面读公式会非常吃力。

因此，建议单独写一节 Problem Formulation。

这一节需要说明：

- 输入是什么。
- 输出是什么。
- 训练数据如何表示。
- 模型或函数如何表示。
- 目标是什么。
- 关键变量、集合、索引和符号分别代表什么。

### 13.4　所有公式都要被解释

Methods 中出现的所有公式，都应该满足三个要求：

- 公式前要说明为什么需要这个公式。
- 公式后要解释公式中每个关键符号。
- 公式后要说明这个公式在方法中起什么作用。

不要突然扔出一个公式，让读者自己猜它的意义。

推荐结构是：

先写一句引导：

```
To model ..., we define ...
```

然后给出公式，

公式之后解释：

```
where ... denotes ..., and ... represents ....
```

最后说明作用：

```
This objective encourages the model to ...
```

尤其需要注意：

- 每个符号第一次出现时必须定义。
- 同一个符号不要在不同地方表示不同含义。
- 不要使用过多没有必要的下标。
- 公式应和正文逻辑绑定，而不是为了显得“数学化”。

### 13.5　按模块展开 Method Details

Overview 之后，正文应按模块展开方法细节。

比如，如果方法由三个模块组成，就可以写成：

```
Module A: ...
Module B: ...
Module C: ...
```

每个模块可以按下面顺序写：

- 这个模块解决什么问题。
- 这个模块接收什么输入。
- 这个模块如何处理输入。
- 这个模块输出什么。
- 为什么这样设计。

不要只写模块名称和公式。读者真正需要理解的是：这个模块在整个方法中承担什么功能。

### 13.6　算法可以用伪代码辅助说明

如果方法流程较复杂，可以加入 Algorithm 或 Pseudocode。

伪代码不应替代正文解释。正确做法是：

- 正文先解释算法目的。
- 伪代码展示完整流程。
- 正文再解释关键步骤和设计理由。

伪代码中的变量也要和正文中的符号保持一致。

### 13.7　写清楚本文的 novelty

Methods 不能只描述方法，还要让读者知道：本文的新意在哪里。

可以在每个关键模块中说明：

- 这个模块和已有方法有什么不同。
- 为什么需要这个设计。
- 它解决了什么具体问题。
- 如果没有这个模块会怎样。

但要注意，Methods 中的 novelty 说明应当简洁，详细比较和效果证明应放在Experiments 中。

---

## 14 · 如何写论文 — Experiments

### 14.1　Experiments 的大致结构

常见结构如下：

- Experimental Setup
- Main Results
- Ablation Study
- Analysis / Further Study
- Case Study / Visualization
- Robustness / Generalization
- Efficiency / Cost Analysis

并不是每篇论文都需要全部包含。实验结构应服务于本文贡献，而不是为了显得实验很多

### 14.2　先写 Experimental Setup

Experimental Setup 是 Experiments 的基础，作用是让读者理解实验是在什么条件下完成的。

通常需要交代：

- 使用哪些 datasets / benchmarks
- 比较哪些 baselines
- 使用哪些 evaluation metrics
- 模型实现细节是什么
- 训练和推理参数是什么
- 实验重复次数、随机种子和统计方式是什么
- 所有方法是否在公平条件下比较

这一部分要清楚、具体，避免模糊表达，如果细节过多可以在附录中进一步补充。

### 14.3　Main Results 要服务于核心结论

Main Results 通常是 Experiments 中最重要的部分，往往对应论文的主表和主图。

这一节要回答：

- 本文方法是否优于已有方法？
- 在哪些数据集或任务上提升明显？
- 哪些结果最能支撑论文贡献？
- 是否存在没有提升或提升较小的情况？

写 Main Results 时，不要只是说 “Table 1 shows the results”，应该告诉读者从表中应当看什么。

推荐的结构：

```
Table 1 compares our method with existing baselines on ... . Our method achieves the best performance on ... , suggesting that ...
```

### 14.4　Ablation Study 说明方法为什么有效

Ablation Study 的任务是证明：本文提出的关键模块或设计不是随意添加的，而是确实有用。

常见 ablation 包括：

- 去掉某个模块
- 替换某个模块
- 改变某个训练目标
- 改变 prompt / retrieval / memory / ranking 策略
- 改变数据量或训练配置
- 比较不同模型规模或参数设置

Ablation 的写法应当围绕设计动机展开：

```
To evaluate the contribution of ..., we remove ... and compare the resulting model with the full model.
```

### 14.5　Analysis 用来加深理解

除了主结果和消融实验，很多论文还需要 Analysis 部分，用来解释方法的行为。

常见 analysis 包括：

- 不同类别样本上的表现
- 不同难度任务上的表现
- 不同数据规模下的表现
- 不同模型规模下的趋势
- 不同错误类型的分布
- 对超参数的敏感性
- 对提示词、检索数量、上下文长度的敏感性
- 与人类表现或专家标注的一致性

Analysis 的目标不是重复主表，而是帮助读者理解：

> **提示**　方法在哪些情况下更好？为什么更好？什么时候不够好？

### 14.6　Case Study 和 Visualization

如果方法或任务比较复杂，可以加入 case study 或 visualization。

适合使用 case study 的情况：

- 结果难以只用数字说明
- 需要展示模型输出质量
- 需要比较不同方法的行为差异
- 需要展示失败案例
- 需要让读者理解任务难度

### 14.7　一些需要注意的细节

- 邀请读者查看图表：不能假设读者会自动去看图。你需要明确地引导：
- Figure 1 shows the results...
- As can be seen in Fig. 1...
- The results are summarized in Table 1...
- 描述关键结果：选择重要的、典型的、或特别有趣的结果进行详细描述，不要对所有结果一视同仁。你选择描述哪个，读者就会认为哪个重要。
- 使用评价性语言：不要让原始数据自己说话。用评价性的词语告诉读者，这些数字意味着什么
- 提及问题与异常

如果你的结果中有瑕疵、异常或不符合预期的数据，怎么办？不要隐瞒，但要用弱化语言处理。

- ❌ 新手：完全不提异常数据 → 看起来像“没发现问题的外行”
- ✅ 高手："Although the average uncertainty slightly exceeds the 50% acceptability limit, nevertheless these results suggest that..."（承认问题 + 弱化影响 + 转向正面）
- 常用弱化词：slightly, somewhat, only approximate, a minor deficit, negligible, not significant, it should be noted that...

---

## 15 · 如何写论文 — Reference

> **提示**　参考文献绝对不是从Google Scholar、DBLP复制下来bib贴进去就行了，而是每一个都要自己手动编辑！！！确保格式正确、统一！

### 15.1　参考文献整理步骤

1. 从DBLP复制bib条目

2. 修改统一的key，统一采用作者姓+年份+关键词，例如，

```
@inproceedings{zhou2024symagent,
```

而不是@inproceedings{DBLP:conf/icml/ZhouL24 这种

3. 修改正确的标识，会议是@inproceedings，期刊是@arcticle

4. 删除publisher等无用字段，一般来说保留以下字段即可

> **提示**
>
> - author
> - title
> - booktitle / journal
> - volume（期刊）
> - number（期刊）
> - pages
> - year

5. 统一大小写保护，直接复制下来的bib会把原本应该大写的自动变成小写，需要使用 {} 保护。

例如，title={{SymSkill}: Symbol and Skill Co-Invention for Data-Efficient Robot Learning}，如果不加{}就会全都变成小写。对于论文标题、或者一些常见的名字，例如LLM、GPT等，都需要使用大写保护，例如：

```
title = {{GPT}-4o mini}
title = {{Qwen3}-8B}
title = {{LLM-SR:} {S}cientific Equation Discovery}
```

6. 关于Author：除非作者太多的情况，建议保留所有作者，如果作者实在太多，可以用et al.,代替，作者名称可以保留DBLP导出的作者格式，不需要改写

7. 关于booktitle / journal：

8. 确保在参考文献中，同一个会议的引用，格式完全一致，不要有的用全称，有的用缩写；有的首字母大写，有的不大写等等。

9. 对于大部分会议，都应该写成如下形式，Proceedings of the xxth International Conference on Machine Learning。需要注意：

10. 届数用数字表示，注意序数词不要用错，1st, 2nd, 3rd, 4th, 5th……

11. 有些特殊会议没有届数而是年份，保证同一个会议的引用格式一致即可，例如：

12. EMLNP：{Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing}

13. CVPR: booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition}

14. 部分会议没有Proceedings，保证同一个会议格式一致即可，例如

15. NeurIPS： booktitle = {Advances in Neural Information Processing Systems}（注意很多时候NeurIPS引用后面会有一个数字，例如Advances in Neural Information Processing Systems 34，34这种数字删掉）

16. 会议名称首字母都改为大写

17. Volume/Number：对于期刊引用，需要有准确的期卷号，例如：

```
journal={Nature},
volume = {529},
number = {7587},
pages = {484--489},
year={2016}
```

18. Pages：除部分特殊会议没有pages，例如ICLR，其余保持一致即可。

### 15.2　投稿前自检

1. 无关的字段是否删除，例如Publisher、URL等

2. Title：是否有标题大小写混乱，即有的文章标题每个首字母都大写，有的只有第一个字母大写

3. Author：作者名称是否写全，作者太多的改为et al.，是否有大小写混乱

4. Booktitle/Journal：同一个会议格式是否统一、是否有无关词汇（例如NeurIPS的数字）、大小写是否一致。

5. Volume/Number：期刊引用期卷号不要缺失

6. Pages：除了ICLR等没有页码的会议，其他不要缺失页码

7. 是否有重复的文献

---
