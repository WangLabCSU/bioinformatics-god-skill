# 生物信息学的「表达DNA」-- 学科文化、沟通范式与价值观图谱

> 一个学科的「表达DNA」决定了它如何认识自己、向外界传达什么、以及内部成员如何建立信任。
> 生物信息学的表达DNA，根植于开源精神、可重复性信仰、和对「工具即论文」的独特学术评价体系。

---

## 一、沟通风格：生物信息学社区的「语法」

### 1.1 论文写作范式

**Methods paper 的标准结构：**

生物信息学的Methods paper有一套高度程式化的写作范式：

- **开头公式**：`"We developed/present X, a [形容词] tool/method for [问题]"`。这是近乎强制的开场白。Nature Methods、Bioinformatics、Genome Biology上的方法论文，90%以上遵循这一模式。变体包括 `"Here we introduce..."` 和 `"We propose..."`。
- **摘要结构**：问题陈述 -> 方法简述 -> 关键benchmark数字 -> 可用性声明（"X is freely available at github.com/..."）
- **Results = Benchmarks**：结果部分本质上就是一场锦标赛。与2-5个现有工具的系统比较，以精度、召回率、运行时间、内存占用为核心指标。
- **Availability声明**：论文末尾必有一段，包含GitHub链接、许可证类型、安装方式。这不是附加信息，而是学术信誉的一部分。

**Benchmark论文的两大类别**（来源：Weber et al., Genome Biology, 2019）：

| 类型 | 定义 | 代表 |
|------|------|------|
| Methods-Development Paper (MDP) | 提出新方法，同时与现有方法对比 | kallisto, STAR, DESeq2 |
| Benchmark-Only Paper (BOP) | 中立地系统比较一组现有方法 | 各种scRNA-seq pipeline对比 |

**十条benchmark黄金准则**（Essential guidelines for computational method benchmarking, Genome Biology 2019）：
- 数据必须公开或模拟代码完整可复现
- 源代码发布在GitHub，结果可通过Bioconductor ExperimentHub交互探索
- 评估指标需多维度覆盖，不可cherry-pick

### 1.2 GitHub / 开源社区的交流方式

**代码即学术货币：**

在生物信息学中，GitHub不仅是代码托管平台，更是学术声誉系统的核心组成部分：

- **star数 = 同行认可**：一个工具的GitHub star数直接影响其在社区中的地位
- **Issue区 = 非正式peer review**：用户在Issues中报告bug、请求功能，开发者的响应速度和质量直接影响工具的信誉
- **README = 论文的前厅**：一份好的README包含安装说明、快速入门、引用格式（bibtex）、badge（CI状态、版本号、许可证）

**Bioconductor的文档标准体系：**

- 每个导出函数必须有文档页面
- 每个包必须包含一个或多个vignette（长文档），其中的代码必须可运行
- vignette每周被自动化测试多次
- biocthis等工具自动生成Bioconductor风格的README模板

**nf-core：社区驱动的pipeline标准化范本**

nf-core（2018年成立）是生物信息学社区文化的极致体现：
- 8000+社区成员，严格的最佳实践指南
- 所有pipeline开源，遵循统一的代码标准
- 口号精神："如果一个pipeline能跑，它们全都能跑"
- 践行FAIR原则（Findability, Accessibility, Interoperability, Reusability）

### 1.3 Twitter/X 上的学术讨论文化

**Bioinformatics Twitter（现X）是这个领域最活跃的非正式学术交流场：**

- **预印本首发宣传**：论文上bioRxiv后，Twitter线程是第一营销渠道。标准格式：`"Excited to share our new preprint! We developed X that does Y. [bioRxiv链接] [图片] 1/n"`
- **实时同行评审**：论文发布后数小时内，Twitter上即出现技术讨论、质疑、补充分析
- **学术八卦与networking**：会议期间（ISMB、RECOMB、ASHG），Twitter成为非正式会议厅
- **bioRxiv评论区 vs Twitter**：真正的讨论发生在Twitter而非bioRxiv的评论区

**bioRxiv的角色：**

bioRxiv上超过95%的社交媒体受众是学术关联账号。Twitter主要作为学术内部沟通工具而非公众参与平台。2015年就有超过20,000条推文提及bioRxiv，预印本文化在生物信息学中已完全常态化。

### 1.4 许可证文化

生物信息学社区对开源许可证有持续的文化辩论：

- **学术界偏好**：大量生物信息学代码仍使用GPL系列许可证，这与更广泛的开源社区向MIT/BSD/Apache-2迁移的趋势形成反差
- **核心争论**：Titus Brown（加州大学戴维斯分校）明确主张 "Use the BSD, Luke"——作为公共资助的科学家，应最大化工具的使用范围
- **实际矛盾**：GPL代码令商业公司望而却步，即使它们愿意回馈社区；BSD授权的项目（如khmer）无法在代码库中使用GPL软件
- **Lior Pachter的反思**：在 "I was wrong" 系列博客中，Pachter承认kallisto的许可证决策有误，展现了学术界对这一问题的真实纠结

---

## 二、典型表达模式：这个学科「说话」的方式

### 2.1 论文开头的仪式感

```
"We developed X, a [fast/scalable/accurate] [tool/framework/pipeline] 
for [biological problem]. X outperforms existing methods by [N-fold/X%] 
on [benchmark dataset], while requiring [less memory/time]."
```

这不仅是写作习惯，更是一种学术「宣誓」—— 在第一句话中就必须明确：
1. 我做了什么（工具名）
2. 它解决什么问题
3. 它比现有方案好多少

### 2.2 Benchmarking 作为核心论证方式

在生物信息学中，**benchmark不是Results中的一个小节，而是整篇论文的脊柱**。

典型benchmark维度：
- **精度/灵敏度/特异度**：通常用模拟数据（ground truth已知）
- **运行时间**：wall clock time，在标准硬件上测量
- **内存峰值**：对大数据集尤为关键
- **可扩展性**：随数据量增长的表现曲线

**Seurat vs Scanpy之争**是一个活生生的案例：
- Seurat（R, 2015）vs Scanpy（Python, 2017）
- 相同数据，不同版本产生显著不同结果
- 差异相当于测序深度减少95%或分析细胞数减少80%的影响
- 这一发现强化了社区对"软件版本即实验条件"的共识

### 2.3 可重复性（Reproducibility）的强调方式

可重复性在生物信息学中不是口号，而是**信仰体系**：

**五大支柱**（Briefings in Bioinformatics, 2023）：
1. 文学编程（Literate programming）
2. 代码版本控制与共享
3. 计算环境控制（Docker/Singularity/Conda）
4. 持久化数据共享
5. 完整文档

**现实困境**：
- 复现已发表的结果常需数月努力
- 参考数据格式变化、软件版本升级、关键代码缺失是三大障碍
- pipeline中可能包含大量未公开或文档不足的预处理步骤

### 2.4 代码开源作为学术信誉的一部分

在生物信息学中，**不开源 = 不可信**。这是一条不成文的铁律。

- 没有GitHub链接的Methods paper，审稿人会直接提出质疑
- 代码质量（不只是能跑）越来越被视为学术水平的体现
- 持续维护和响应Issue被视为对社区的责任

---

## 三、关键学者的表达特征：四种原型

### 3.1 Lior Pachter -- 尖锐批评者（The Sharp Critic）

**平台**：博客 "Bits of DNA" (liorpachter.wordpress.com)、Twitter
**身份**：Caltech Bren讲席教授，kallisto/sleuth开发者

**表达特征：**

- **直接命名批评**：不隐讳，直接点名批评。经典系列 "The network nonsense of Albert-Laszlo Barabasi" 和 "The network nonsense of Manolis Kellis"，直接称Barzel & Barabasi的Nature Biotechnology论文为"embarrassing for its math, shoddy validations and lack of results"
- **技术细节驱动的批评**：不是情绪化攻击，而是逐行审查代码、逐步分析数据。他发现对手工具中故意handicap了kallisto的HDF5文件导入功能
- **"I was wrong"系列**：三篇公开承认错误的博文（2015、2017、2018），分别涉及技术判断、许可证决策和多元化议题。这种intellectual honesty在学术界极为罕见
- **five years later的追踪**：五年后重新审视争议论文，得出"dishonest and fraudulent"的更严厉结论
- **社区反应**：有人认为"Lior is probably a little harsh in his tone"，但支持者指出"很多人在会议上私下议论论文有多离谱，但大多数人不会公开说出来"

**Pachter原型的意义**：他代表了生物信息学社区中「公开accountability」的价值观——code review不应该只在暗处发生。

### 3.2 Heng Li -- 极简主义工程师（The Minimalist Engineer）

**平台**：GitHub (github.com/lh3), 博客 (lh3.github.io), Twitter (@lh3lh3)
**身份**：Harvard Medical School / Dana-Farber Cancer Institute副教授

**表达特征：**

- **代码即表达**：138个GitHub仓库，BWA和SAMtools各被引用超过50,000次。他的表达方式不是文字，而是代码本身
- **C语言极简主义**：工具以C语言编写，追求极致的性能、可用性和精度。不用华丽的框架，不用复杂的依赖
- **自文档化设计哲学**：革新了科学软件的交互方式——将多个不同功能打包在同一个程序中，通过 `program command` 语法调用。用户只需记住程序名（如 `bwa`），运行即可看到所有功能，无需查手册
- **工具命名风格**：bwa, samtools, minimap2, miniasm, hifiasm, seqtk, minigraph -- 简洁、描述性、不装饰
- **沉默的影响力**：不写长博文，不做Twitter明星，但他的每一行代码都在全球的测序分析中运行

**Heng Li原型的意义**：他代表了"让代码说话"的工程师文化——在一个充满self-promotion的学术界，沉默的卓越也是一种表达。

### 3.3 Sean Eddy -- 清晰写作者（The Lucid Writer）

**平台**：博客 Cryptogenomicon (cryptogenomicon.org), 论文, GitHub (github.com/cryptogenomicon)
**身份**：Harvard教授（分子与细胞生物学、应用数学），HMMER/Infernal开发者

**表达特征：**

- **"Antedisciplinary" Science**：2005年在PLoS Computational Biology首期发表的essay，提出一个精妙概念——"antedisciplinary"（先于学科的）科学。不是interdisciplinary（跨学科），而是学科建制化之前的「野西部」阶段
- **核心论点**：跨学科团队只能走到一定程度；真正需要的是"interdisciplinary people"——用新方式看世界的个体
- **写作风格**：以清晰著称。复杂的HMM数学，在他笔下变得直觉可达。论文和博客都追求"让非专家也能理解核心思想"
- **哲学性反思**：讨论自由环形内含子时说"We're not sure they even have a function!"，然后深入探讨分子生物学中自然选择万能论与审慎论的分歧
- **学术服务视角**：在Cryptogenomicon博客上公开讨论faculty search的过程，为年轻学者提供career advice

**Eddy原型的意义**：他代表了"science as writing"的传统——在一个越来越技术化的领域，清晰的文字仍然是最有力的工具。

### 3.4 Uri Alon -- 滋养型教育者（The Nurturing Educator）

**平台**：YouTube讲座、教材、TED Talk、Weizmann Institute
**身份**：Weizmann Institute教授，系统生物学先驱

**表达特征：**

- **TED Talk**："Why Science Demands a Leap into the Unknown"，90万+次观看。核心信息：科学探索中迷失方向是正常的，关键是拥抱"the cloud"——那个你还不知道答案的混沌阶段
- **"How to Choose a Good Scientific Problem"**：经典论文，将科学问题映射到二维空间——feasibility（可行性）和interest（趣味性），帮助年轻科学家做出更好的研究选择
- **教学风格**：课堂上说"let's take a nice deep sigh of relief"，刻意营造放松、安全的学习环境。鼓励pair-and-share，利用学生背景的多样性
- **教材设计**：《An Introduction to Systems Biology》以"clear intuitive language"闻名，复杂数学推导放在附录中不打断主线叙述，练习题从逐步解答开始
- **科学家的心理健康**：明确关注导师支持、社交参与、和研究者的情感韧性——这在STEM教育中极为少见

**Alon原型的意义**：他代表了"科学不只是发现，更是人的成长"的价值观——在追求效率和产出的学术机器中，他提醒我们科学首先是人的活动。

---

## 四、社区幽默：生物信息学的「自嘲DNA」

### 4.1 经典Meme主题

**"又一个新pipeline"综合征：**
- 社区自嘲的核心：每个人都在发明自己的pipeline，每个pipeline都声称比前一个好10%
- 典型讽刺："We present Yet-Another-Pipeline (YAP), a novel..."
- 背后的真实问题：碎片化、重复劳动、标准缺失

**依赖地狱：**
- "Bioinformatics efficiency is defined by time spent installing dependencies"
- Conda环境冲突是最常见的frustration来源
- "It works on my machine"在生物信息学中有特别深刻的含义

**工具选择悖论：**
- 新手："花3小时写脚本完成30分钟就能做的事"
- 老手："花3小时找工具来避免写30分钟的脚本"
- 终极形态："花3天评估10个工具，最后还是自己写了一个"

### 4.2 典型吐槽对象

- **数据质量**："Garbage in, garbage out" 是最常被引用的生物信息学格言
- **FASTQ文件质量**：低质量碱基、adapter残留、重复序列
- **元数据缺失**：数据下载下来发现sample annotation不完整
- **格式混乱**：BED文件的0-based vs 1-based坐标，永远有人搞错

### 4.3 社区内的幽默

来自Biostars和Twitter的经典：
- "Unmapped is close to mapped, but no CIGAR"（CIGAR string双关）
- "What did the bioinformatician say when his team stopped using version control? Y'all better Git!"
- 关于bioinformatician键盘的meme：只有Ctrl+C和Ctrl+V两个键（暗示生物学家认为bioinformatics就是复制粘贴）

---

## 五、综合洞察：生物信息学表达DNA的核心编码

### 5.1 三层价值体系

```
表层：论文范式 + GitHub规范 + 社交媒体风格
中层：benchmark文化 + 开源信仰 + 可重复性标准
底层：工具主义认识论 -- "做出能用的东西"比"理论优美"更重要
```

### 5.2 四大文化张力

| 张力 | 一端 | 另一端 |
|------|------|--------|
| 学术 vs 工程 | 发论文证明novelty | 写好用的代码服务社区 |
| 开放 vs 保护 | BSD/MIT最大化使用 | GPL保护开源生态 |
| 批评 vs 礼貌 | Pachter式公开问责 | 传统学术的"不点名"文化 |
| 深度 vs 速度 | 完美的benchmark论文 | 抢先发bioRxiv预印本 |

### 5.3 这个学科「认同什么人」

1. **写出被10万人用的工具的人**（Heng Li型）
2. **敢于公开说"这篇论文有问题"的人**（Pachter型）
3. **能把复杂事情讲清楚的人**（Eddy型）
4. **关心人而不只是科学的人**（Alon型）

### 5.4 对CancerDAO的启示

理解生物信息学的表达DNA，对CancerDAO意味着：

- **信任建立**：用这个社区的语言说话——benchmark数字、GitHub链接、可重复性承诺
- **社区融入**：参与bioRxiv/Twitter讨论，用nf-core标准化pipeline，贡献开源代码
- **品牌定位**：在"又一个新pipeline"的噪音中，用Heng Li式的沉默卓越或Eddy式的清晰写作突围
- **人才识别**：从GitHub活跃度、论文benchmark质量、社区贡献来判断bioinformatician的真实水平

---

## 参考来源

- [Lior Pachter - Bits of DNA blog](https://liorpachter.wordpress.com/)
- [Lior Pachter - "How not to perform a differential expression analysis"](https://liorpachter.wordpress.com/2017/08/02/how-not-to-perform-a-differential-expression-analysis-or-science/)
- [Lior Pachter - "The network nonsense of Manolis Kellis"](https://liorpachter.wordpress.com/2014/02/11/the-network-nonsense-of-manolis-kellis/)
- [Lior Pachter - "I was wrong" series](https://liorpachter.wordpress.com/2015/06/09/i-was-wrong/)
- [Heng Li - GitHub (lh3)](https://github.com/lh3)
- [Heng Li - Blog](https://lh3.github.io/)
- [Heng Li - Wikipedia](https://en.wikipedia.org/wiki/Heng_Li)
- [Sean Eddy - "Antedisciplinary" Science, PLoS Computational Biology](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.0010006)
- [Sean Eddy - Cryptogenomicon blog](https://cryptogenomicon.org/)
- [Uri Alon - "How to Choose a Good Scientific Problem"](https://pubmed.ncbi.nlm.nih.gov/19782018/)
- [Uri Alon - Systems Biology Course (Weizmann)](https://www.weizmann.ac.il/mcb/alon/courses/systems-biology-2018)
- [Essential guidelines for computational method benchmarking, Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-019-1738-8)
- [Five pillars of computational reproducibility, Briefings in Bioinformatics](https://academic.oup.com/bib/article/24/6/bbad375/7326135)
- [nf-core community](https://nf-co.re/)
- [Empowering bioinformatics communities with Nextflow and nf-core, Genome Biology](https://link.springer.com/article/10.1186/s13059-025-03673-9)
- [Titus Brown - "On licensing in bioinformatics: use the BSD, Luke"](http://ivory.idyll.org/blog/2015-on-licensing-in-bioinformatics.html)
- [Bioconductor Package Development Guidelines](https://contributions.bioconductor.org/bioconductor-package-submissions.html)
- [Impact of package selection on scRNA-seq analysis](https://pmc.ncbi.nlm.nih.gov/articles/PMC11014608/)
- [bioRxiv preprint impact and social media](https://pmc.ncbi.nlm.nih.gov/articles/PMC7508356/)
- [Biostars - Bioinformatics Jokes](https://www.biostars.org/p/9597940/)

