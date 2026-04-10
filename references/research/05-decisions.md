# 生物信息学关键决策、里程碑与转折点

> 记录改变生物信息学领域方向的决策、工具设计哲学、学术-产业分叉、以及失败教训。

---

## 一、改变整个领域方向的决策

### 1.1 Bermuda Principles (1996)：数据必须公开

**背景**：1996年2月，人类基因组计划（HGP）领导人在百慕大召开战略会议。此前，基因组数据的发布遵循传统学术惯例——数据在论文发表后才公开。

**关键决策**：与会者达成共识：所有人类基因组序列数据必须在产生后24小时内释放到公共数据库。这一原则彻底颠覆了生物学数据共享的传统。

**推动者**：
- **John Sulston** 和 **Robert Waterston**（线虫生物学家）将 *C. elegans* 社区的日常数据共享实践引入 HGP
- NIH 和 Wellcome Trust 共同资助了 HGP 90% 的测序工作，为执行该原则提供了制度保障

**实际影响**：
- 德国、日本、法国等国的公共资助数据政策必须做出例外调整以适应 Bermuda Principles
- 日常共享最初的目的是务实的——质量控制和项目协调——但最终创造了生物医学研究数据开放的全新范式
- 被认为是 HGP 最重要的遗产之一

**深层意义**：Bermuda Principles 证明了一个反直觉的命题：在大科学项目中，放弃数据独占权反而能加速整体进展。这一原则的精神延续到了后来的 ENCODE、1000 Genomes、Human Cell Atlas 等项目。

> 参考：[The Bermuda Triangle (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC7307446/) | [Bermuda Principles (Wikipedia)](https://en.wikipedia.org/wiki/Bermuda_Principles)

---

### 1.2 UCSC Genome Browser 的开源决策 (2000)

**背景**：2000年，Celera Genomics 正试图将人类基因组数据商业化并申请基因专利。

**关键人物**：Jim Kent，UCSC 研究生，在导师 David Haussler 指导下工作。

**决策与行动**：
- 2000年5月，Kent 放下所有其他工作，集中精力解决基因组组装问题——他的核心动机是**阻止 Celera 及其客户锁定大部分人类基因组的专利**
- 2000年7月7日，UCSC 在线发布了首个人类基因组工作草图，同时推出 Genome Browser 的初始版本
- Browser 作为图形化的网页"显微镜"，向任何人免费开放

**开源模式**：
- 完整源代码开源（GitHub: ucscGenomeBrowser/kent）
- 学术和非营利用户可免费使用代码在内部服务器重建浏览器
- 商业用户需支付许可费

**深层意义**：UCSC Genome Browser 的开源不仅是技术选择，更是一种**政治行动**——通过让数据和工具先于商业实体公开，事实上使得基因组数据的商业垄断变得不可能。

> 参考：[Jim Kent (Wikipedia)](https://en.wikipedia.org/wiki/Jim_Kent) | [UCSC Genome Browser History](https://genome.ucsc.edu/goldenPath/history.html)

---

### 1.3 ENCODE 项目：启动与争议 (2003-2012)

**项目启动**：ENCODE（Encyclopedia of DNA Elements）由 NHGRI 于2003年启动，目标是建立人类基因组中所有功能元件的全面目录。

**引爆争议的声明 (2012)**：ENCODE 团队在 Nature 发表论文，声称人类基因组的 **80.4%** 具有"生化功能"（biochemical function）。媒体迅速将其解读为"垃圾 DNA 已死"。

**核心争论——"功能"的定义**：
- **ENCODE 立场**：只要一段 DNA 能与转录因子结合、被甲基化修饰、或被转录为 RNA，就算有"功能"
- **批评者立场**（Dan Graur 等）：这种定义混淆了"生化活性"和"进化功能"。人类基因组中保守的 DNA 远不足以支撑 80% 的功能声明。Graur 发表了措辞激烈的论文 "On the Immortality of Television Sets"，系统批驳 ENCODE 的功能定义
- **哲学维度**：斯坦福哲学百科专门收录了 ENCODE 争议，指出项目忽略了生物哲学家和理论生物学家在"功能"概念上的关键工作

**后续发展**：ENCODE 核心成员在回应中不再提及 80.4% 这一数字，承认创建一个开放获取的资源"远比对基因组功能比例的任何临时估计更重要"。

**教训**：
1. 大科学项目的公关声明需要与科学严谨性匹配
2. 概念的精确定义（什么是"功能"？）是生物信息学的核心挑战
3. 数据资源的价值可以与最初的解读框架分离

> 参考：[Stanford Encyclopedia of Philosophy - ENCODE](https://plato.stanford.edu/entries/genomics/encode-project.html) | [Is Junk DNA Bunk? (PNAS)](https://www.pnas.org/doi/10.1073/pnas.1221376110) | [Graur et al. (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC3622293/)

---

### 1.4 Human Cell Atlas 项目 (2016-)

**发起**：2016年，由 **Aviv Regev**（Broad Institute / MIT）和 **Sarah Teichmann**（Sanger Institute）共同提出并发起。首次会议于2016年10月在伦敦召开。

**项目愿景**：利用单细胞基因组学、蛋白质组学、转录组学等技术，为人体每一种细胞类型建立全面的参考图谱。

**规模与治理**：
- 2017年在以色列正式启动，初始联盟包含130多名科学家
- 由35人组成的国际组织委员会领导
- 截至2024年，已将约6200万人类细胞映射到18个生物网络中

**战略意义**：
- 是单细胞革命从技术驱动转向系统性工程的标志
- Regev 后来加入 Genentech，证明该领域的学术积累已具备直接的产业价值
- 开创了大规模国际协作的新范式——不像 HGP 集中在少数大型中心，HCA 采用分布式、网络化的协作模式

> 参考：[Human Cell Atlas (Nature)](https://www.nature.com/articles/550451a) | [HCA Official](https://www.humancellatlas.org/learn-more/about-the-human-cell-atlas/)

---

### 1.5 AlphaFold 开源：AI 进入结构生物学 (2018-2024)

**CASP13 (2018)**：DeepMind 的 AlphaFold 首次参加蛋白质结构预测竞赛，在43个最难目标中25个获得最佳预测，中位 GDT 分数 58.9。

**CASP14 (2020)**：AlphaFold 2 实现质的飞跃——97个目标中88个获最佳预测，中位 GDT 分数达到 **92.4/100**。被广泛认为"解决"了蛋白质折叠问题。AlphaFold 2 采用了全新的端到端可微分架构，与2018版本有根本不同。

**开源决策及其复杂性**：
- **AlphaFold 2**（2021）：在科学界强烈要求下，DeepMind 开源了代码和方法细节。Nature 论文附带60页补充信息
- **AlphaFold DB**：与 EMBL-EBI 合作，预测了超过 **2亿** 蛋白质结构，覆盖几乎所有已知蛋白质，并免费开放
- **AlphaFold 3**（2024）：争议性地拒绝开源长达6个月。最终于2024年11月为学术界开放代码和权重（仅限非商业用途）

**影响**：
- 超过300万研究者在190多个国家使用 AlphaFold
- 2024年 Nobel 化学奖授予 Demis Hassabis 和 John Jumper（与 David Baker 共享）
- 加速了药物发现、抗菌素耐药性研究、作物韧性和心脏病等方向的研究

**深层意义**：AlphaFold 3 的开源延迟揭示了一个核心张力——AI 公司在"为科学造福"和"保持商业竞争优势"之间的持续拉扯。这种张力在未来的 AI for Science 领域只会更加尖锐。

> 参考：[AlphaFold (Wikipedia)](https://en.wikipedia.org/wiki/AlphaFold) | [DeepMind Blog](https://deepmind.google/blog/alphafold-a-solution-to-a-50-year-old-grand-challenge-in-biology/)

---

## 二、关键工具/方法的设计决策

### 2.1 BLAST：速度与灵敏度的经典权衡 (1990)

**设计背景**：1990年，Altschul 等人开发了 BLAST（Basic Local Alignment Search Tool），面对的核心挑战是——GenBank 数据库持续增长，穷举搜索在计算上不可行。

**核心设计哲学**："通过牺牲灵敏度来换取速度"。BLAST 不做全局比对，只搜索序列中最显著的模式。

**关键权衡参数**：
- **邻域词得分阈值**（neighborhood word-score threshold）：阈值越高 → 速度越快 → 越可能遗漏相关序列
- 用户应使用"对当前任务足够灵敏的最快参数集"

**技术演进**：
- 原始 BLAST (1990)：词对种子，无空位比对
- BLAST2 / Gapped BLAST：降低邻域词得分阈值以维持灵敏度，同时支持空位比对
- BLAST 比 FASTA 更快，因为它只搜索最显著的模式

**深层意义**：BLAST 的设计哲学——"good enough, fast enough"——成为生物信息学工具设计的典范。它证明了在海量数据场景中，精确最优解往往不如快速近似解实用。

> 参考：[BLAST (Wikipedia)](https://en.wikipedia.org/wiki/BLAST_(biotechnology)) | [Having a BLAST (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC138974/)

---

### 2.2 BWA / Bowtie 选择 BWT 算法 (2008-2009)

**技术背景**：二代测序（NGS）产生海量短读段（short reads），需要高效地将它们比对到参考基因组。传统的哈希表方法（如 MAQ）面临内存瓶颈。

**BWT 算法的引入**：
- **Bowtie**（Ben Langmead, 2008年8月首次发布）：率先将 Burrows-Wheeler Transform (BWT) 和 FM-Index 引入基因组比对。BWT 的核心优势是通过 FM-Index 大幅压缩内存占用，同时支持高效的精确匹配
- **BWA**（Heng Li, 2009年发表）：同样基于 BWT，但在处理错配（mismatches）和空位（gaps）方面更灵活

**为什么选择 BWT？**
- BWT-FM Index 允许在压缩的索引上直接搜索，无需将整个基因组加载到内存
- 对于人类基因组（~3GB），BWT 索引可以将内存需求控制在几 GB 以内
- Ferragina & Manzini (2000) 的理论工作为此提供了算法基础

**BWA vs Bowtie 的分化**：
- Bowtie / Bowtie2：更快，适合短读段和 RNA-seq（通过 TopHat/HISAT2 扩展）
- BWA-MEM：对较长读段（>70bp）和配对端（paired-end）reads 更准确，成为变异检测的标准工具
- BWA 经历了 BWA-backtrack → BWA-SW → BWA-MEM 三代演进

**深层意义**：BWT 的引入是计算机科学理论直接改变生物信息学实践的经典案例。一个1994年的数据压缩算法，通过2000年的 FM-Index 理论扩展，在2008年成为解决 NGS 数据分析瓶颈的关键。

> 参考：[BWA Paper (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC2705234/) | [Bowtie2 Manual](https://bowtie-bio.sourceforge.net/bowtie2/manual.shtml)

---

### 2.3 SAM/BAM 格式标准的制定 (2008)

**诞生背景**：2008年初，1000 Genomes Project 启动时，市场上已有许多短读段比对器和变异检测工具，每个工具有自己的输入/输出格式——互操作性为零。

**Heng Li 的闪电式开发**：
- 2008-11-14：实现 BGZF（Block GZip Format）
- 2008-11-18：BAM on RAZF 可工作
- 2008-11-20：实现分箱（binning）和线性索引
- 2008-11-21：实现 sort/merge/pileup/faidx 以及 tview 原型
- 2008-12-08：向 1000 Genomes 发送最终草案
- 2008-12-22：samtools 首次公开发布

**从一个月到十年的标准**：从动手到公开发布只用了约5周，但 SAM/BAM 成为了统治十年以上的行业标准。

**设计要点**：
- CIGAR 字符串（表示比对细节）改编自 Guy Slater 的 Exonerate，但 Heng Li 扩展了操作符
- BAM 使用 BGZF 压缩，支持随机访问——这是处理大规模基因组数据的关键特性
- 1000 Genomes Project 以 SAM/BAM 格式发布所有比对数据，迅速建立了正反馈

**深层意义**：SAM/BAM 的成功证明了标准制定的两条铁律：(1) 标准的采用速度与大型项目的背书直接相关；(2) 配套工具（samtools）与格式同时发布，是标准被快速接受的关键。

> 参考：[Heng Li's Blog - Early History of SAM/BAM](http://lh3.github.io/2015/01/27/the-early-history-of-the-sambam-format) | [SAMtools Paper (Bioinformatics)](https://academic.oup.com/bioinformatics/article/25/16/2078/204688)

---

### 2.4 Heng Li 的性能哲学：为什么总是 C

**核心人物**：Heng Li，哈佛医学院副教授，其论文（SAMtools, BWA）各被引用超过 50,000 次（截至2025年10月）。

**工具清单**：BWA, samtools, minimap2, seqtk, htslib, bwa-mem2...几乎全部用 C 编写。

**编程语言哲学**：
- 当前组合是"C + JavaScript"——一个快语言搭配一个脚本语言
- 他自己说"不推荐别人学这个组合"
- 选择 C 的根本原因：生物信息学的核心瓶颈是 I/O 和内存。C 提供对两者的直接控制
- 与 Python 生态的差异：Python 适合快速原型和数据科学工作流，但在处理 TB 级基因组数据时性能差距可达10-100倍

**minimap2 的设计哲学**：
- 核心目标：速度、适应性、精度
- 同时支持短读段（Illumina）和长读段（Oxford Nanopore, PacBio）
- 单一工具取代了多个专用工具

**深层意义**：Heng Li 代表了生物信息学中"工程师-科学家"的典范——他的工具不是发论文的副产品，而是精心设计的基础设施。他对性能的执着源于一个实际判断：在基因组数据指数增长的时代，算法效率是科学产出的速率限制步骤。

> 参考：[Heng Li's Blog](https://lh3.github.io/) | [Heng Li (Wikipedia)](https://en.wikipedia.org/wiki/Heng_Li)

---

### 2.5 Seurat vs Scanpy：R 与 Python 的路线分叉

**两条路线**：
| 维度 | Seurat | Scanpy |
|------|--------|--------|
| 语言 | R | Python |
| 首次发布 | 2015 | 2017 |
| 核心数据结构 | SeuratObject | AnnData |
| 生态系统 | Bioconductor, Monocle | NumPy, SciPy, PyTorch |
| 扩展性 | 模块化，与 R 生态深度集成 | 内存优化，面向大规模数据 |

**技术差异的实际影响**：
- 同一数据在 Seurat 和 Scanpy 中的差异表达分析结果可以有显著差异
- 差异程度相当于对基准数据集测序不到5%的reads、或分析不到20%的细胞群体
- 不同版本的同一工具也能产生截然不同的结果

**社区分化的深层原因**：
- Seurat 出自 Satija Lab（纽约基因组中心），深度嵌入统计学/生物学 R 传统
- Scanpy 出自 Theis Lab（Helmholtz Munich），深度嵌入机器学习/Python 传统
- 这不仅是工具选择，而是两种研究文化的表达

**深层意义**：Seurat 和 Scanpy 的共存证明了生物信息学一个不变的真相——没有"客观最优"的分析流程。工具选择本身就是方法论假设的一部分。可重复性不仅取决于数据和算法，还取决于软件版本、参数默认值和实现细节。

> 参考：[Scanpy vs Seurat (Data Science For Bio)](https://datascienceforbio.com/scanpy-vs-seurat/) | [Impact of Package Selection (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11014608/)

---

## 三、学术界 vs 产业界的关键分叉

### 3.1 Craig Venter vs 公共基因组计划 (1998-2003)

**竞赛起源**：
- 1990年：HGP 正式启动，国际公共联盟
- 1990年代初：Venter 从 NIH 辞职，转向基因组商业化
- **1998年**：Venter 宣布成立 Celera Genomics，计划用全基因组鸟枪法（whole-genome shotgun）在2001年前完成人类基因组测序，并仅向付费客户开放数据。同时计划为6000+基因申请初步专利

**商业模式的威胁**：Celera 的模式直接挑战了 Bermuda Principles 的精神——如果基因组数据被锁定在付费墙后面，整个公共生物学研究体系都将受限。

**竞赛的加速效应**：Celera 的进入反而加速了公共项目——HGP 比原计划提前两年完成。

**政治解决**：
- 2000年，白宫介入调停
- 2000年6月26日，克林顿总统主持联合声明，宣布两方都完成了人类基因组工作草图
- 2001年2月，两方在 Nature 和 Science 分别发表论文

**后续**：
- 2002年1月，Venter 从 Celera 离职
- 2003年，HGP 发布"黄金标准"序列
- Celera 的商业模式最终失败——当公共数据免费可用时，付费数据库无法维持

**深层意义**：这场竞赛是"开放科学 vs 知识产权"之争的原型案例。最终结果证明：在基础科学数据领域，**公共开放模式具有不可逆转的优势**——一旦数据公开，商业围墙就无法重新建立。

> 参考：[Nature (2020)](https://www.nature.com/articles/d41586-020-01849-w) | [yourgenome.org](https://www.yourgenome.org/theme/why-was-there-a-race-to-sequence-the-human-genome/)

---

### 3.2 23andMe 的兴衰：消费级基因组学的商业化之路 (2006-2025)

**崛起**：
- 2006年成立，2008年被 Time 评为"年度发明"
- 核心创新：将基因组检测价格从 $1,000 降到 $99，单日售出17,000-18,000套
- 长期战略目标：建立大规模生物样本库，用于医学研究和可专利发现

**FDA 危机 (2013)**：
- 2013年11月，FDA 发出警告信，要求立即停止营销
- 核心问题：公司与 FDA 从2009年就开始谈判，但2013年5月**突然停止与 FDA 沟通**，同时继续营销产品
- FDA 担忧：假阳性结果导致不必要的治疗，假阴性导致重大风险被忽视
- 结果：2013-2015年仅提供祖源报告，健康报告被暂停

**逐步恢复**：
- 2015年：FDA 批准 Bloom 综合征等携带者状态报告
- 2017年：批准阿尔茨海默病、帕金森病等遗传健康风险报告
- 2018年：首个 FDA 批准的 DTC 癌症风险基因检测（BRCA1/BRCA2）

**终局——破产与数据危机 (2025)**：
- 2021年上市后估值60亿美元
- 股价暴跌95%+，药物开发部门失败
- **2025年3月23日**：申请破产
- 核心争议：1500万+用户的基因数据何去何从？
- TTAM Research Institute 以3.05亿美元收购基因数据库
- 参议员提出《Don't Sell My DNA Act》，要求转移基因数据前须获得用户书面同意
- 联邦层面缺乏保护：HIPAA 不适用于 DTC 公司

**深层教训**：
1. 基因数据是"终身唯一"的——不像密码可以更改，一旦泄露无法撤回
2. 商业模式建立在用户数据上的公司，其破产意味着数据资产的所有权危机
3. 消费级基因组学的最大风险不是技术，而是监管框架的缺失

> 参考：[NPR (2025)](https://www.npr.org/2025/03/24/nx-s1-5338622/23andme-bankruptcy-genetic-data-privacy) | [Scientific American](https://www.scientificamerican.com/article/23andme-bankruptcy-leaves-troves-of-genetic-data-at-risk/)

---

### 3.3 华大基因（BGI）：中国基因组学的国家冠军 (1999-)

**起源**：1999年由王健、于军、杨焕明、刘思奇在北京创立，最初目的是参与 HGP。

**关键转折 (2010)**：
- 购买128台 Illumina HiSeq 2000 测序仪
- 获得中国国家开发银行15亿美元的十年"合作资金"
- 一举成为全球最大的 NGS 测序中心

**商业化路径**：
- 2012年开始商业化服务
- 发展模式："研发-生产-应用"一体化
- 自主研发测序平台（MGISEQ/DNBSEQ），摆脱对 Illumina 的依赖
- 2017年在深圳证券交易所上市
- 国际扩张：美国（Cambridge）、欧洲（Copenhagen）

**争议与地缘政治**：
- 被比作生物技术领域的华为
- 享受研发补贴、出口融资、外交支持和国内采购保障
- 引发西方对基因数据安全的担忧

**深层意义**：BGI 代表了一种完全不同于西方的生物技术发展路径——国家意志驱动、规模化优先、产学研一体化。这种模式的长期竞争力取决于能否从"测序工厂"转向真正的科学创新。

> 参考：[BGI Group (Wikipedia)](https://en.wikipedia.org/wiki/BGI_Group) | [Chinese Institute Makes Bold Sequencing Play (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC7097335/)

---

### 3.4 DeepMind 进入蛋白质折叠领域

参见 [1.5 AlphaFold 开源]。

**补充要点——为什么是 DeepMind？**
- 蛋白质折叠预测是计算生物学的50年老问题，传统方法（基于物理的分子动力学模拟）进展缓慢
- DeepMind 的优势不在生物学知识，而在**大规模深度学习工程能力**
- CASP13 到 CASP14 的飞跃证明：问题的瓶颈不是生物学理论，而是计算方法
- 这标志着 AI 公司开始在基础科学领域与学术界直接竞争——而且赢了

---

### 3.5 Aviv Regev 加入 Genentech (2020)

**背景**：Aviv Regev 在 Broad Institute 工作14年，是单细胞基因组学的开创者之一，Human Cell Atlas 的共同发起人。

**关键决策**：2020年5月，Regev 接受了 Genentech Research and Early Development 执行副总裁的职位。

**为什么这件事重要**：
- Regev "并没有在找新工作"——Broad Institute 之外没有她想去的学术机构
- Genentech/Roche 的offer 不同寻常：他们选了一位**计算和系统生物学家**而非传统的临床科学家来领导研发
- 这意味着大型制药公司开始认为：单细胞基因组学和计算生物学不再只是学术工具，而是**药物开发的核心能力**

**象征意义**：Regev 的转型是学术界-产业界人才流动的标志性事件。当一个领域的顶尖学者愿意离开最好的学术平台转向产业界，说明该领域的产业化拐点已经到来。

> 参考：[MIT Biology](https://biology.mit.edu/aviv-regev-to-join-genentech-in-august/) | [Fierce Biotech](https://www.fiercebiotech.com/biotech/genentech-lures-regev-from-broad-institute-to-lead-research-and-early-development)

---

## 四、失败与教训

### 4.1 Jesse Gelsinger 事件：基因治疗的至暗时刻 (1999)

**患者背景**：Jesse Gelsinger，17岁，患有鸟氨酸转氨甲酰酶（OTC）缺乏症。通过严格的非蛋白饮食，病情控制良好。他是自愿参加试验的，希望帮助新生儿患者。

**致命试验**：
- 1999年9月13日，研究人员将携带正常 OTC 基因的腺病毒载体注射到他的肝动脉
- Gelsinger 出现严重免疫反应
- 4天后死亡

**暴露的系统性问题**：
1. **知情同意失败**：Gelsinger 未被告知其他患者已出现严重副作用，也未被告知3只猴子在注射后死于凝血障碍和重度肝炎
2. **入组标准违反**：Gelsinger 的肝功能检测结果不佳，按标准不应入组
3. **利益冲突**：首席科学家 James Wilson 与正在使用的腺病毒载体有经济利益关系

**后果**：美国所有基因治疗试验一度暂停。该事件使基因治疗领域停滞近十年。

**教训**：
- 知情同意不能只是法律文件——必须真正让受试者理解风险
- 利益冲突会腐蚀科学判断
- 安全性数据的透明共享是临床试验伦理的底线

> 参考：[Science History Institute](https://www.sciencehistory.org/stories/magazine/the-death-of-jesse-gelsinger-20-years-later/) | [NYU Bioethics](https://med.nyu.edu/departments-institutes/population-health/divisions-sections-centers/medical-ethics/education/high-school-bioethics-project/learning-scenarios/jesse-gelsinger-case)

---

### 4.2 法国 X-SCID 基因治疗：成功与灾难共存 (1999-2008)

**背景**：Alain Fischer 和 Marina Cavazzana-Calvo 领导的巴黎团队，使用逆转录病毒载体治疗 X-连锁重症联合免疫缺陷（X-SCID）婴儿。

**初始成功**：11名接受治疗的男孩中，9名免疫系统成功恢复。

**灾难性并发症**：
- 2002年10月：第1例患儿发展为白血病样 T 细胞增殖
- 3个月后：第2例白血病
- 最终：9名治愈患者中**4人**在治疗后31-68个月发展为 T 细胞白血病
- 机制：逆转录病毒载体插入 LMO2 原癌基因附近，激活其转录 → 插入性突变致癌

**后续影响**：
- 巴黎团队暂停试验
- 德国、意大利、美国监管机构暂停类似基因转移试验
- 推动了对更安全载体（如慢病毒载体、AAV）的研发

**深层教训**：
- 基因治疗的"治愈"和"致癌"可以同时发生在同一个试验中
- 随机插入的逆转录病毒载体是一个定时炸弹——插入位点的随机性意味着风险不可完全预测
- 这一事件直接推动了基因编辑技术（CRISPR 等）的发展——精确编辑可以避免随机插入的风险

> 参考：[JCI Paper](https://www.jci.org/articles/view/35700) | [2002 French Gene Therapy Trials (Wikipedia)](https://en.wikipedia.org/wiki/2002_French_gene_therapy_trials)

---

### 4.3 GWAS 的 "Missing Heritability" 问题 (2008-)

**问题的发现**：2008年由 Maher 首次命名。核心矛盾：

| 估计方法 | 遗传贡献度 |
|----------|-----------|
| 双生子/家系研究 | 50-70%（行为特征），80%（身高） |
| GWAS 发现的变异 | 1-5%（行为特征），~5%（身高，早期） |

**具体案例**：家系研究表明人类身高80%由遗传决定，但早期 GWAS 发现的约50个身高相关变异只能解释5%的身高变异。

**提出的解释**：
1. **多基因架构 + 统计功效不足**（2010年论文证实）：大量小效应变异在当时的样本量下无法检测到——这被证明是主要原因
2. **罕见变异**（频率 < 0.5%）：需要全基因组测序而非 SNP 芯片
3. **上位性**（基因间交互作用）：非加性遗传效应难以在 GWAS 框架中捕获
4. **双生子研究高估遗传率**：违反等环境假设

**解决进展**：随着样本量从万级增长到百万级（如 UK Biobank），GWAS 能解释的遗传变异比例大幅提高。但"missing heritability"仍然部分存在。

**深层教训**：
- 统计关联 ≠ 因果机制
- 复杂性状的遗传架构远比"一个基因一个表型"复杂
- GWAS 的"失败"实际上推动了对多基因风险评分（PRS）和全基因组测序的发展

> 参考：[Missing Heritability (Wikipedia)](https://en.wikipedia.org/wiki/Missing_heritability_problem) | [Three Legs of the Missing Heritability (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC9172633/)

---

### 4.4 个人基因组学的早期过度承诺 (2007-2013)

**承诺**：DTC 基因检测公司宣称，基因风险测试可以"赋能消费者"、为个人身份提供有价值的输入、并预测复杂疾病风险（心血管病、癌症等）。

**现实**：
- 2010年，FDA 向多家 DTC 公司发出警告信
- GAO 报告裁定检测结果"具有误导性，几乎没有实际用途"，三分之二的被调查公司"从事某种形式的欺诈性、欺骗性或可疑的营销行为"
- 许多公司退出市场或从纯 DTC 模式转向医生合作模式

**研究证据**：
- 既没有支持者预期的健康行为改善，也没有批评者担心的灾难性心理伤害
- 但30-45%的参与者在检测后报告自我效能感降低
- 主要问题：多因素复杂疾病的基因风险预测在当时的技术水平下确实"几乎没有临床价值"

**深层教训**：
- 技术可行性（能测基因）≠ 临床有效性（测了有用）≠ 临床实用性（改变了行为/结局）
- 消费者直接获取基因信息的模式需要配套的教育和咨询体系
- 基因决定论的过度宣传会反噬——当消费者发现基因预测并不"准确"时，信任崩塌

> 参考：[DTC-GT Review (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC3777821/) | [DTC Failure Is Not an Option (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC3086846/)

---

### 4.5 Duke/Potti 丑闻：可重复性危机的标志性案例 (2006-2012)

**虚假研究**：从2006年起，Anil Potti 和 Joseph Nevins 在 Nature Medicine、NEJM 等顶级期刊发表一系列论文，声称可以利用肿瘤细胞的基因活性模式来预测最有效的化疗药物。

**问题暴露**：
- NCI 工作人员无法重现 Duke 的结果
- 数据和文档不完整，需要"法医生物信息学"（forensic bioinformatics）才能推断出原始分析过程
- Keith Baggerly 和 Kevin Coombes 发表了经典的"法医生物信息学"分析，系统揭露了数据操纵

**临床危害**：
- 基于错误分析的临床试验在2007-2010年间进行
- 患者可能被给予了错误的药物
- Duke 被8个受影响患者家庭起诉，庭外和解

**系统性影响**：
- 美国医学研究所（IOM）专门研究基因组学在临床试验中的使用规范，2012年发布报告
- 报告要求：研究者必须公开用于开发临床测试的**数据、计算机代码和计算程序**
- 直接推动了可重复研究运动（reproducible research movement）

**深层教训**：
1. 生物信息学分析的"黑箱"特性使欺诈更难被发现
2. 代码和数据的公开不是"锦上添花"，而是科学诚信的基本要求
3. 同行评审在高度计算化的研究中严重失效——审稿人通常不审查代码
4. "法医生物信息学"应该成为常规实践，而非事后补救

> 参考：[Duke Scandal (JNCI)](https://academic.oup.com/jnci/article/103/12/916/2607218) | [Anil Potti (Wikipedia)](https://en.wikipedia.org/wiki/Anil_Potti) | [Baggerly & Coombes Analysis](https://pmc.ncbi.nlm.nih.gov/articles/PMC138974/)

---

## 附录：时间线总览

| 年份 | 事件 | 类型 |
|------|------|------|
| 1990 | BLAST 发布 | 工具 |
| 1990 | 人类基因组计划启动 | 里程碑 |
| 1996 | Bermuda Principles 确立 | 决策 |
| 1998 | Celera Genomics 成立 | 分叉 |
| 1999 | Jesse Gelsinger 死亡 | 失败 |
| 1999 | BGI 成立 | 分叉 |
| 2000 | UCSC Genome Browser 上线 | 决策 |
| 2000 | 人类基因组工作草图发布 | 里程碑 |
| 2002 | 法国 X-SCID 白血病事件 | 失败 |
| 2003 | ENCODE 项目启动 | 里程碑 |
| 2006 | 23andMe 成立 | 分叉 |
| 2006 | Duke/Potti 虚假论文开始发表 | 失败 |
| 2008 | Bowtie 发布（BWT 引入比对） | 工具 |
| 2008 | GWAS "Missing Heritability" 命名 | 教训 |
| 2008 | SAM/BAM 格式制定 | 工具/标准 |
| 2009 | BWA 发表 | 工具 |
| 2010 | BGI 购买128台 HiSeq 2000 | 分叉 |
| 2010 | DTC 基因检测遭 FDA/GAO 打击 | 失败 |
| 2012 | ENCODE "80% functional" 争议 | 教训 |
| 2013 | 23andMe 被 FDA 要求停止营销 | 失败 |
| 2015 | Seurat 发布 | 工具 |
| 2016 | Human Cell Atlas 发起 | 里程碑 |
| 2017 | Scanpy 发布 | 工具 |
| 2018 | AlphaFold CASP13 夺冠 | 里程碑 |
| 2020 | AlphaFold 2 CASP14 突破 | 里程碑 |
| 2020 | Aviv Regev 加入 Genentech | 分叉 |
| 2021 | AlphaFold 2 开源 | 决策 |
| 2024 | AlphaFold Nobel Prize | 里程碑 |
| 2024 | AlphaFold 3 开源（非商业） | 决策 |
| 2025 | 23andMe 破产 | 失败/教训 |

---

*最后更新：2026-04-10*
