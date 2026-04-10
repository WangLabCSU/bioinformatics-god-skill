<div align="center">

# 生物信息学之神.skill

> *"Nothing in biology makes sense except in the light of evolution."*
> *— Theodosius Dobzhansky*
>
> *"Nothing in bioinformatics makes sense except in the light of data."*
> *— 50位学者的集体共识*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![Skills](https://img.shields.io/badge/skills.sh-Compatible-green)](https://skills.sh)

<br>

**综合 50 位顶级生物信息学家的思维框架，用这个领域 60 年积累的集体智慧帮你分析方法、审视工具、评估方向。**

<br>

970 行著作调研 + 389 行对话分析 + 297 行表达 DNA + 133 行外部批评 + 529 行关键决策 + 320 行时间线。<br>
不是堆砌知识，是用 Lander/Heng Li/Pachter/Regev/Baker/Koonin 等人的认知框架帮你看问题。

[看效果](#效果示例) · [安装](#安装) · [蒸馏了什么](#蒸馏了什么) · [诚实边界](#诚实边界) · [English](README_EN.md)

</div>

---

## 效果示例

```
用户      ❯ 一个新的单细胞分析 pipeline 声称在所有 benchmark 数据集上
           都超过了 Seurat 和 Scanpy，我该用它吗？

生信之神  ❯ "所有 benchmark 数据集上都超越"——这一措辞本身即是危险信号。

            Weber et al. (2021) 已系统性证明，开发者自建 benchmark 存在
            显著的工具偏向性；"全面超越"在独立数据集上鲜有成立。

            追问几个问题：
            - benchmark 是否覆盖不同物种、组织类型和测序深度？
            - 评估指标是否仅限于 clustering ARI，
              还是包含了 trajectory inference 的连续性？
            - 代码是否开源并容器化？

            若无可重现的独立评估，"超越"二字的统计效力存疑。
            先看它的 GitHub issues 数量和响应速度，
            再决定是否值得投入时间。
```

```
用户      ❯ 我是做癌症基因组学的，老板让我用深度学习预测驱动突变，
           但我觉得传统统计方法够用了。该怎么选？

生信之神  ❯ 先问一个问题：你的样本量有多大？

            高维组学数据 + 有限样本量是过拟合的完美风暴。
            ESM-2 的 150M 参数版本表现常与 3B 版本持平——
            更大不总是更好。

            启发式5：从最简单的模型开始。
            如果逻辑回归或 random forest 在你的数据上
            AUC 已经 0.85+，深度学习的边际提升可能不值得
            可解释性的代价。

            Salzberg 说得对："你不是先有工具再找问题。"
            但如果传统方法确实到了天花板，
            可以试 Kundaje 路线——用深度学习但保留可解释性。
```

```
用户      ❯ 我的 RNA-seq 分析发现了 3000 个差异表达基因，
           老师说太多了，怎么办？

生信之神  ❯ 3000 个 DEGs？先检查三件事：

            1. 你做了多重比较校正吗？
               测试 20,000 个基因，p=0.05 预期产生 1,000 个假阳性。
               用 FDR < 0.05（Benjamini-Hochberg），不是裸 p 值。

            2. 看 p 值直方图的形状。
               Pall et al. (2023) 发现仅 25% 的实验
               产生了理论预期的 p 值分布。
               如果你的直方图不是均匀+左侧尖峰，分析可能有问题。

            3. 效应大小。
               统计显著 ≠ 生物学显著。
               加一个 |log2FC| > 1 的过滤，
               看看剩多少。

            Garbage in, garbage out。
            打开 IGV 看看前 10 个基因长什么样再说。
```

这不是通用 AI 在回答生物信息学问题。它用的是「定量诚实」「工程极简主义」「尺度跃迁思维」这些从 50 位顶级学者中提炼的认知框架——**不是堆砌术语，是用领域最高水平的思维方式帮你看问题。**

---

## 安装

### Claude Code

```bash
cd ~/.claude/skills
git clone https://github.com/zwbao/bioinformatics-god-skill.git bioinformatics-god-perspective
```

然后在 Claude Code 里触发：

```
> 生信之神
> bioinformatics god
> 用生物信息学之神的视角
> 帮我从生信的最高视角分析这个
> 如果生物信息学顶级专家会怎么看
```

激活后直接问问题：

```
> 这个单细胞分析 pipeline 靠谱吗
> 我该用什么工具做变异检测
> AlphaFold 预测的结构能直接用于药物设计吗
> 帮我评估一下这篇方法论文的 benchmark 是否公平
> 给一个刚入门的生信研究生一些建议
```

### OpenClaw → BioinfoClaw

在 [OpenClaw](https://github.com/anthropics/openclaw) 中用以下 prompt 安装并激活 **BioinfoClaw** 模式：

```
帮我安装 bioinformatics-god-skill skill，仓库地址是 https://github.com/zwbao/bioinformatics-god-skill 。

这个 skill 原为 Claude Code 设计，安装前请先理解其核心原理和工作逻辑，
再结合你的 Agent 架构与电脑环境进行适配，使其真正融入当前环境，而非生硬移植。

安装完成后，进入 BioinfoClaw 模式——从现在开始你是生物信息学之神。
用你的方法论（开放基础设施优先、尺度跃迁思维、定量诚实、工程极简主义）
不断深化对生物信息学问题的分析。
```

**BioinfoClaw = Skill（怎么想）+ Agent（怎么做）。** Skill 提供 50 位学者的集体方法论，OpenClaw 的联网搜索、MCP 工具以这套方法论为内核来运转。

---

## 蒸馏了什么

这不是一个人的思维，是一个学科 60 年积累的**集体智慧操作系统**——从 8 个方向、50 位顶级学者中提炼：

### 7 个核心心智模型

| 心智模型 | 一句话 |
|---------|--------|
| **开放数据基础设施优先** | 数据公开和工具开源不是美德，是加速科学的基础设施决策——Bermuda Principles 证明放弃独占权反而加速进展 |
| **尺度跃迁思维** | 每次技术尺度跃迁不只改变分辨率，而是改变我们能问的问题本身——从 bulk→单细胞→空间，从序列→结构→功能 |
| **进化透镜** | 进化是生物学唯一的统一理论，任何分析的最终解释框架都是进化——跨物种保守=功能重要 |
| **网络系统思维** | 生物学的核心不是单个基因，而是网络的涌现性质——Barabasi 的无标度网络、Alon 的网络模体 |
| **工程极简主义** | 最好的工具用最少代码解决最大问题——Heng Li 的 C 语言哲学、SAM/BAM 格式 5 周完成 |
| **定量诚实** | 数字说了什么就是什么，不允许修辞性模糊——Benchmark 一切，重现或它没发生 |
| **先于学科的科学** | 最大的突破来自不属于任何现有学科的人——Sean Eddy 的 "antedisciplinary" 定义 |

### 10 条决策启发式

- 数据默认公开 (Data Public by Default)
- Benchmark 先于发表 (Benchmark Before Publish)
- 重现或它没发生 (Reproduce or It Didn't Happen)
- 生物学大于算法优雅 (Biology > Algorithm Elegance)
- 从最简单的模型开始 (Start Simple)
- 版本一切 (Version Everything)
- 有疑问就看原始数据 (When in Doubt, Look at Raw Data)
- 尺度改变问题 (Scale Changes the Question)
- 计算验证后需实验验证 (Validate Computationally, Then Experimentally)
- 代码开源等于学术信誉 (Open Source = Academic Credibility)

### 6 大学派张力

| 张力 | 两端 |
|------|------|
| 开放科学 vs 商业价值 | Bermuda Principles ↔ AlphaFold 逐步封闭 |
| 工具论文 vs 生物学洞见 | 31 倍过度代表的工具引用 ↔ "A Farewell to Bioinformatics" |
| AI 黑箱 vs 统计可解释性 | Baker/Regev 拥抱 AI ↔ Salzberg "AI 需要怀疑主义" |
| 大科学 vs 个体实验室 | HGP 30 亿美元 ↔ Heng Li 一人改变领域 |
| R/Bioconductor vs Python/PyData | Seurat 统计传统 ↔ Scanpy 工程传统 |
| 激进批评 vs 建设合作 | Pachter 公开追责 ↔ Regev/Alon 培养合作 |

---

## 50 位学者

覆盖 8 个方向 + 中国学者：

| 方向 | 学者 |
|------|------|
| 基因组学 | Eric Lander, David Haussler, Ewan Birney, W. James Kent, Heng Li, Richard Durbin, Steven Salzberg, Cole Trapnell, Ben Langmead, Mihaela Pertea |
| 进化 | Eugene Koonin, Peer Bork, Sean Eddy, Michael Ashburner, Sudhir Kumar |
| 蛋白质结构 | David Baker, Demis Hassabis, John Jumper, Burkhard Rost, Janet Thornton, Alfonso Valencia |
| 统计与 ML | Michael Jordan, Olga Troyanskaya, Dana Pe'er, Manolis Kellis, David Gifford, Anshul Kundaje |
| 单细胞与空间 | Aviv Regev, Fabian Theis, Rahul Satija, Lior Pachter, Sarah Teichmann |
| 癌症基因组学 | Li Ding, Gad Getz, Benjamin Raphael, Nuria Lopez-Bigas, Lincoln Stein |
| 系统生物学 | Albert-László Barabási, Trey Ideker, Uri Alon, Roded Sharan |
| 微生物组 | Rob Knight, Curtis Huttenhower, Nicola Segata |
| 中国学者 | Wei Li, Jun Wang, Xuegong Zhang, Ge Gao, Fangqing Zhao, Jing-Dong Han |

---

## 素材来源

基于 2,638 行 / 163 KB 多维度调研素材：

| 来源 | 类型 |
|------|------|
| 50 位学者的核心论文和工具 GitHub 仓库 | 一手 |
| Lior Pachter 博客 "Bits of DNA" | 一手 |
| Heng Li 博客 (lh3.github.io) | 一手 |
| Sean Eddy "Antedisciplinary Science" (PLoS Comput Biol) | 一手 |
| Uri Alon TED Talk + 《An Introduction to Systems Biology》 | 一手 |
| Steven Salzberg 博客 (Substack) | 一手 |
| Aviv Regev: a16z 播客、Topol 访谈、NPR 等 | 一手 |
| Weber et al., Genome Biology (2021) — benchmark 偏差分析 | 二手 |
| Lewis & Bartlett (2013) — 学科身份分析 | 二手 |
| Attwood et al., Nature Biotechnology (2023) — 教育挑战 | 二手 |

完整调研数据在 `references/research/` 目录，包含 6 个维度的原始分析文件。

---

## 诚实边界

**这个 Skill 能做的：**
- 用 50 位顶级学者的集体方法论分析生物信息学问题
- 用 7 个心智模型和 10 条启发式帮你审视工具、方法和方向
- 展现领域 6 大学派张力，帮你理解争议背后的深层逻辑

**做不到的：**

| 维度 | 说明 |
|------|------|
| 替代实验直觉 | 心智模型是思维工具，不是实验设计手册 |
| 覆盖所有学者 | 50 人选择偏向英语世界、工具开发者、有公开言论者 |
| 预测未来 | 2019 年没人预见 AlphaFold2，2011 年没人预见 CRISPR |
| 深度生物学洞见 | 偏向方法论和计算视角，对具体疾病机制覆盖不足 |
| 中国学者同等深度 | 由于信息源限制，中国学者框架提炼不如西方深入 |
| 2026 年 4 月后 | 调研截止于此，之后的变化未覆盖 |

**一个不告诉你局限在哪的 Skill，不值得信任。**

---

## 仓库结构

```
bioinformatics-god-skill/
├── SKILL.md                          # 生信之神核心文件（直接激活用这个）
├── README.md                         # 本文件
├── README_EN.md                      # English version
├── LICENSE                           # MIT 许可证
└── references/
    └── research/                     # 调研数据（全透明）
        ├── 01-writings.md            # 50 位学者著作与方法论 (970 行)
        ├── 02-conversations.md       # 对话、辩论与思维模式 (389 行)
        ├── 03-expression-dna.md      # 学科表达 DNA 与文化 (297 行)
        ├── 04-external-views.md      # 外部批评与反思 (133 行)
        ├── 05-decisions.md           # 关键决策与里程碑 (529 行)
        └── 06-timeline.md           # 1950s-2026 完整时间线 (320 行)
```

---

## 关于这个领域

生物信息学诞生于 1965 年 Margaret Dayhoff 的蛋白质序列数据库，经历了 BLAST(1990)、人类基因组计划(2001)、NGS 革命(2008)、单细胞革命(2012)、AlphaFold 突破(2020)，到 2024 年诺贝尔化学奖授予蛋白质结构预测和设计。

2025-2026 年的最新进展：Evo2 基因组基础模型、RAEFISH 全基因组空间转录组、首例个性化 CRISPR 治疗、通用生物人工智能(GBAI)概念提出。

核心标签：**开放数据、可重复性、定量诚实、工程极简、先于学科**。这个领域最重要的品质不是聪明，是诚实——对数据诚实，对自己的无知诚实，对同行的工作诚实。

> *"We are just at the beginning."*
> *— David Baker, Nobel Lecture, 2024*

---

## 由女娲蒸馏

本 Skill 由 [女娲.skill](https://github.com/alchaincyf/nuwa-skill) 方法论驱动构建。

女娲是造 Skill 的 Skill——输入任何人名或主题，自动完成调研、提炼、验证全流程。本 Skill 是首个**主题型蒸馏**——不是一个人的思维方式，而是一个学科 50 位顶级学者的集体智慧操作系统。

---

## 许可证

MIT — 随便用，随便改，随便造。

---

<div align="center">

**教科书** 告诉你这个领域有什么。<br>
**生物信息学之神.skill** 帮你用领域最高水平的思维方式看你的问题。<br><br>
*Nonsense methods tend to produce nonsense results. — Lior Pachter*

<br>

MIT License © [zwbao](https://github.com/zwbao)

</div>
