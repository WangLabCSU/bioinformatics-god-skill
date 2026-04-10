# 生物信息学完整时间线：从诞生到2026年

> 本文档按年代梳理生物信息学领域的关键事件，标注影响程度（**开创性** / **重要** / **补充**），并在时间线上定位50位核心学者的贡献。
>
> 最后更新：2026-04-10

---

## 一、1950s-1960s：序曲与萌芽

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 1953 | Watson & Crick 发表 DNA 双螺旋结构 | **开创性** — 奠定分子生物学基础，生物信息学的逻辑前提 | **James Watson**, **Francis Crick**, Rosalind Franklin |
| 1955 | Frederick Sanger 完成胰岛素氨基酸全序列测定 — 人类历史上第一个蛋白质完整序列 | **开创性** — 证明蛋白质有确定的化学结构，开启序列生物学 | **Frederick Sanger** |
| 1962 | Zuckerkandl & Pauling 提出"分子钟"假说 — 通过比较血红蛋白序列推断物种分化时间 | **重要** — 将序列分析与进化理论连接，奠定分子进化学 | **Emile Zuckerkandl**, **Linus Pauling** |
| 1965 | Margaret Dayhoff 出版《Atlas of Protein Sequence and Structure》— 收录当时已知的全部65条蛋白质序列 | **开创性** — 生物信息学的"创世之作"；建立了第一个生物序列数据库；发明氨基酸单字母编码系统 | **Margaret Dayhoff** |
| 1966 | Dayhoff 开发 PAM 矩阵（Point Accepted Mutation）— 第一个氨基酸替换矩阵 | **开创性** — 序列比对评分体系的基础，至今影响所有比对算法的设计思想 | **Margaret Dayhoff** |
| 1969 | 首次用计算机重建蛋白质进化树（Dayhoff 团队） | **重要** — 计算进化生物学的起点 | **Margaret Dayhoff** |

---

## 二、1970s：算法奠基

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 1970 | Needleman-Wunsch 算法发表 — 基于动态规划的全局序列比对 | **开创性** — 生物信息学第一个核心算法；动态规划思想此后贯穿整个领域 | **Saul Needleman**, **Christian Wunsch** |
| 1972 | Walter Fiers 团队首次完成 RNA 基因全序列（MS2噬菌体外壳蛋白基因） | **重要** — 核酸序列测定的先驱工作 | Walter Fiers |
| 1975 | Sanger 发明双脱氧链终止法（Sanger 测序法） | **开创性** — 统治 DNA 测序领域30年，人类基因组计划的技术基础 | **Frederick Sanger** |
| 1977 | Sanger 完成噬菌体 phiX174 全基因组测序（5,375 nt）— 第一个完整测序的DNA基因组 | **开创性** — 基因组学的诞生 | **Frederick Sanger** |
| 1978 | 蛋白质数据银行（PDB）建立 — 从最初的7个结构开始 | **开创性** — 结构生物信息学的基石，至今仍是蛋白质结构的核心资源 | 布鲁克海文国家实验室团队 |

---

## 三、1980s：基础设施建设

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 1981 | Smith-Waterman 算法发表 — 局部序列比对的最优解 | **开创性** — 发现序列中的局部相似区域，功能域识别的理论基础 | **Temple Smith**, **Michael Waterman** |
| 1982 | GenBank 在 Los Alamos 国家实验室建立 | **开创性** — 核酸序列的"中央银行"，至今是最重要的公共序列数据库 | |
| 1983 | Kary Mullis 发明 PCR（聚合酶链式反应） | **开创性** — 虽非直接的生信方法，但PCR使序列数据爆炸式增长，推动了对生信工具的需求 | **Kary Mullis** |
| 1984 | SWISS-PROT 数据库建立（现 UniProt） | **重要** — 手工注释的蛋白质序列数据库，质量标杆 | **Amos Bairoch** |
| 1985 | FASTA 算法发表 — 第一个快速序列相似性搜索工具 | **重要** — 在BLAST之前的标准序列搜索方法 | **William Pearson**, **David Lipman** |
| 1987 | 隐马尔可夫模型（HMM）引入序列分析 | **重要** — 蛋白质家族建模、基因预测的理论基础；后被 HMMER、Pfam 等广泛采用 | **Gary Churchill**, **David Haussler** |
| 1988 | 美国国家生物技术信息中心（NCBI）成立 | **开创性** — 成为全球最大的生物信息资源中心 | **David Lipman**（首任主任） |
| 1988 | FASTA格式成为事实标准 | **补充** — 简单但持久的序列文件格式 | **William Pearson** |

---

## 四、1990s：基因组时代开启

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 1990 | BLAST 算法发表 | **开创性** — 生物信息学使用最广的工具，没有之一；启发式方法平衡速度与灵敏度 | **Stephen Altschul**, **David Lipman**, **Webb Miller**, **Eugene Myers**, Warren Gish |
| 1990 | 人类基因组计划（HGP）正式启动 — 30亿美元、15年计划 | **开创性** — 生物学史上最大的单一研究项目，彻底重塑了生物信息学 | **Francis Collins**, **James Watson**（初期负责人） |
| 1991 | EST（表达序列标签）方法发表 — 快速基因发现策略 | **重要** — 以低成本快速识别基因，推动功能基因组学 | **Craig Venter** |
| 1992 | BLOSUM 替换矩阵发表 — 从局部比对块中导出的替换矩阵 | **重要** — 取代 PAM 矩阵成为 BLAST 默认评分矩阵 | **Steven Henikoff**, **Jorja Henikoff** |
| 1993 | Sanger Centre（现 Wellcome Sanger Institute）建立 | **重要** — 承担HGP约三分之一的测序工作 | **John Sulston** |
| 1994 | Pfam 蛋白质家族数据库发布 — 基于 HMM 的蛋白质域分类 | **重要** — 蛋白质功能注释的标准工具 | **Sean Eddy**, **Erik Sonnhammer**, Alex Bateman |
| 1995 | 第一个自由生活有机体全基因组测序完成（流感嗜血杆菌，*H. influenzae*） | **开创性** — 全基因组鸟枪法测序的验证；比较基因组学的起点 | **Craig Venter**, **Hamilton Smith**, **Claire Fraser** |
| 1996 | 酿酒酵母全基因组完成 — 第一个真核生物基因组 | **开创性** — 真核基因组注释方法学的建立 | 国际酵母基因组合作组 |
| 1997 | HMMER 发表 — 基于 profile HMM 的序列分析软件 | **重要** — 蛋白质家族搜索的金标准工具 | **Sean Eddy** |
| 1998 | 线虫 *C. elegans* 基因组完成 — 第一个多细胞动物基因组 | **开创性** — 发育生物学与基因组学的结合 | **John Sulston**, **Robert Waterston**, **Sydney Brenner** |
| 1998 | 全基因组鸟枪法测序策略提出（用于人类基因组） | **重要** — 挑战了逐步克隆方法，加速了测序竞赛 | **Craig Venter**, **Eugene Myers** |
| 1999 | 人类22号染色体全序列完成 — HGP的第一条完成的常染色体 | **补充** — 技术里程碑 | Sanger Centre 团队 |

---

## 五、2000s：后基因组时代

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 2000 | 果蝇 *Drosophila melanogaster* 基因组发表 — 鸟枪法的大规模验证 | **重要** — 证实全基因组鸟枪法适用于复杂基因组 | **Craig Venter**, **Gerald Rubin**, **Eugene Myers** |
| 2001 | 人类基因组草图同时发表（Nature & Science） | **开创性** — 基因数量远低于预期（~20,000-25,000），颠覆"一个基因一个蛋白"的简单观点；开启后基因组时代 | **Francis Collins**（公立HGP）, **Craig Venter**（Celera） |
| 2002 | 小鼠基因组完成 — 人类疾病模型基因组 | **重要** — 比较基因组学的关键参考 | Mouse Genome Sequencing Consortium |
| 2003 | 人类基因组计划正式完成 — 覆盖率达99%，错误率低于万分之一 | **开创性** — 耗资27亿美元的里程碑 | **Francis Collins** 等 |
| 2003 | David Baker 团队用计算方法从头设计出 Top7 — 第一个非自然蛋白质 | **开创性** — 计算蛋白质设计的突破，开启理性蛋白质工程新时代 | **David Baker** |
| 2003 | ENCODE 项目启动 — 目标：识别人类基因组中所有功能元件 | **开创性** — 从"基因组是什么"走向"基因组做什么" | **Ewan Birney**, NHGRI |
| 2004 | 下一代测序（NGS）技术问世 — 454 Life Sciences 发布第一台商业化 NGS 平台 | **开创性** — 将测序成本降低数个数量级，使组学研究民主化 | Jonathan Rothberg |
| 2005 | 国际 HapMap 项目第一阶段完成 — 100万个 SNP 位点 | **重要** — GWAS的基础设施 | 国际 HapMap 联盟 |
| 2006 | Illumina Solexa 测序平台发布 | **开创性** — 最终成为NGS市场的主导平台，产生了全球绝大多数测序数据 | Illumina / Solexa |
| 2007 | 1000 Genomes Project 启动 — 目标：建立人类遗传变异综合图谱 | **重要** — 群体基因组学的里程碑 | |
| 2008 | RNA-seq 方法学发表 — 用NGS进行转录组分析 | **开创性** — 取代微阵列成为基因表达分析的金标准 | **Barbara Wold**, Ali Mortazavi 等 |
| 2008 | Bowtie 短读比对工具发表 | **重要** — 开创了基于 BWT/FM-index 的超快比对算法时代 | **Ben Langmead**, **Cole Trapnell**, Steven Salzberg |
| 2009 | TopHat 发表 — 第一个支持剪接比对的 RNA-seq 工具 | **重要** — 使 RNA-seq 能够发现新的剪接事件 | **Cole Trapnell**, Ben Langmead, Steven Salzberg |
| 2009 | BWA 发表 — 另一个主流短读比对工具 | **重要** — 与 Bowtie 并列为最广泛使用的比对软件 | **Heng Li** |

---

## 六、2010s 前半：大数据基因组学

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 2010 | SAMtools/BCFtools 框架成熟 — 变异检测的标准流程 | **重要** — 定义了变异检测的工业标准 | **Heng Li** |
| 2010 | 1000 Genomes Project 第一阶段数据发布 | **重要** — 第一次系统性绘制人群级变异图谱 | 1000 Genomes Consortium |
| 2010 | DESeq 发表 — RNA-seq 差异表达分析 | **重要** — 统计方法进入组学数据分析 | **Wolfgang Huber**, Simon Anders |
| 2011 | GATK（Genome Analysis Toolkit）广泛采用 | **重要** — 变异检测的"黄金标准"流水线 | Broad Institute, **Mark DePristo** |
| 2012 | ENCODE 项目大规模结果发表 — 30篇论文同时发表 | **开创性** — 揭示基因组中约80%有功能活性（此结论引发争议），重新定义了"垃圾DNA" | **Ewan Birney** 等 |
| 2012 | CRISPR-Cas9 基因编辑技术发表 | **开创性** — 生命科学领域最具变革性的技术之一；极大推动了功能基因组学研究 | **Jennifer Doudna**, **Emmanuelle Charpentier**, **Feng Zhang** |
| 2012 | 单细胞 RNA-seq（scRNA-seq）方法学快速发展（Smart-seq 等） | **开创性** — 打破了"批量平均"的局限，揭示细胞异质性 | **Rickard Sandberg**, **Sten Linnarsson** |
| 2013 | TCGA（The Cancer Genome Atlas）进入成果爆发期 — 覆盖33种癌症类型 | **开创性** — 癌症基因组学的最大公共资源；重新定义了癌症分类 | NCI/NHGRI, **Li Ding** 等 |
| 2013 | Galaxy 平台广泛采用 — 无代码的生信分析平台 | **重要** — 降低了生物信息学的使用门槛 | **Anton Nekrutenko**, **James Taylor** |
| 2013 | Oxford Nanopore 发布 MinION — 掌上纳米孔测序仪 | **重要** — 开启实时、长读长、便携测序时代 | Oxford Nanopore Technologies |
| 2014 | Drop-seq / inDrop 发表 — 高通量 scRNA-seq | **开创性** — 将单细胞测序成本降低100倍，从数百细胞提升到数万细胞 | **Evan Macosko**, **Allon Klein**, **Steven McCarroll** |

---

## 七、2010s 后半：单细胞与深度学习

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 2015 | 1000 Genomes Project 最终数据集发布 — 2,504个个体的变异目录 | **重要** — 群体遗传学的基准数据集 | 1000 Genomes Consortium |
| 2015 | CRISPR 筛选（大规模功能基因组学）兴起 | **重要** — 高通量鉴定基因功能 | **Feng Zhang**, **David Sabatini** |
| 2016 | 10x Genomics Chromium 平台推出 — 商业化高通量 scRNA-seq | **开创性** — 使单细胞分析成为常规实验，推动了 Human Cell Atlas 等大型项目 | 10x Genomics |
| 2016 | DeepVariant 项目启动 — Google 将深度学习引入变异检测 | **重要** — CNN 在基因组学中的标志性应用 | Google Health / **Mark DePristo** |
| 2017 | Human Cell Atlas（HCA）项目正式启动 — 目标：绘制人体每一种细胞类型的图谱 | **开创性** — 被称为"细胞版的人类基因组计划" | **Aviv Regev**, **Sarah Teichmann** |
| 2017 | Scanpy 发表 — Python 生态的单细胞分析框架 | **重要** — 成为 scRNA-seq 分析的标准工具之一（与 R 的 Seurat 并列） | **Fabian Theis**, Alex Wolf |
| 2017 | 长读长测序技术成熟（PacBio SMRT + Nanopore） | **重要** — 解决了结构变异检测、重复区域装配等短读长的盲区 | PacBio, Oxford Nanopore |
| 2018 | Seurat v3 发表 — R 生态的单细胞分析标准 | **重要** — 定义了 scRNA-seq 分析的标准流程（QC → 归一化 → 聚类 → 标记基因） | **Rahul Satija** |
| 2018 | UMAP 取代 t-SNE 成为单细胞降维可视化的首选 | **补充** — 更好地保留全局结构 | Leland McInnes |
| 2019 | 单细胞多组学（scATAC-seq, CITE-seq 等）快速发展 | **重要** — 从单一转录组扩展到多维度细胞画像 | 多个团队 |
| 2019 | Perturb-seq 规模化 — CRISPR 筛选 + 单细胞读出 | **重要** — 高分辨率功能基因组学 | **Jonathan Weissman**, **Aviv Regev** |
| 2019 | 人类泛基因组参考联盟（HPRC）成立 | **重要** — 从单一参考基因组走向多样化参考 | T2T/HPRC 团队 |

---

## 八、2020-2022：AI 革命开启

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 2020 | AlphaFold2 在 CASP14 中取得突破 — 蛋白质结构预测达到实验精度 | **开创性** — 解决了困扰生物学50年的蛋白质折叠问题；被认为是 AI 在科学领域最重要的突破之一 | **Demis Hassabis**, **John Jumper** (DeepMind) |
| 2020 | 单细胞 ATAC-seq + RNA-seq 联合分析（多组学）普及 | **重要** — 同时测量转录组和表观基因组 | 10x Genomics, 多个团队 |
| 2020 | COVID-19 疫情加速了基因组监测和生信基础设施建设 | **重要** — 病毒基因组学、系统发育追踪、mRNA疫苗设计全面依赖生信工具 | Nextstrain 团队, **Trevor Bedford** 等 |
| 2020 | Emmanuelle Charpentier & Jennifer Doudna 获诺贝尔化学奖（CRISPR） | **开创性** — 基因编辑获最高学术认可 | **Jennifer Doudna**, **Emmanuelle Charpentier** |
| 2021 | AlphaFold Protein Structure Database 上线 — 覆盖98.5%的人类蛋白质预测结构 | **开创性** — 免费开放2亿+蛋白质结构预测，极大加速了结构生物学研究 | **Demis Hassabis**, **John Jumper** |
| 2021 | ESM（Evolutionary Scale Modeling）蛋白质语言模型发表 | **重要** — 用 Transformer 架构学习蛋白质序列的进化规律 | **Alexander Rives** (Meta AI) |
| 2021 | 空间转录组学方法爆发（Visium, MERFISH, seqFISH+） | **开创性** — 在保留空间信息的同时测量基因表达，被 Nature Methods 评为年度技术 | **Xiaowei Zhuang**（MERFISH）, 10x Genomics（Visium）|
| 2022 | T2T（Telomere-to-Telomere）完整人类基因组发表 — 无间隙覆盖全部染色体 | **开创性** — 新增约2亿碱基对的新序列，包括99个编码基因；首次完整解析着丝粒、端粒和重复区域 | **Karen Miga**, **Adam Phillippy**, **Evan Eichler** |
| 2022 | ESMFold 发表 — 仅用语言模型即可预测蛋白质结构（不依赖MSA） | **重要** — 证明蛋白质语言模型隐含了结构信息 | **Alexander Rives** (Meta AI) |
| 2022 | RoseTTAFold 发表 — David Baker 团队的结构预测模型 | **重要** — AlphaFold 的开源替代方案 | **David Baker** |
| 2022 | Cellxgene Census 上线 — CZI 的大规模单细胞数据门户 | **重要** — 标准化的数亿细胞数据集 | Chan Zuckerberg Initiative |

---

## 九、2023-2024：多模态 AI 与精准医学

| 年份 | 事件 | 影响 | 关键学者 |
|------|------|------|----------|
| 2023 | 人类泛基因组参考发布（HPRC 首批47个基因组） | **开创性** — 从单一参考走向多样化参考基因组，解决了参考偏差问题 | **Evan Eichler**, **Benedict Paten**, HPRC 联盟 |
| 2023 | DNABERT-2 / Nucleotide Transformer 等基因组语言模型发表 | **重要** — 将 NLP 的大模型范式引入 DNA 序列理解 | 多个团队 |
| 2023 | scGPT 等单细胞基础模型发表 — Transformer 架构处理单细胞数据 | **重要** — 探索预训练范式在单细胞分析中的潜力 | **Bo Wang** 等 |
| 2023 | Compressed Perturb-seq 发表 — 大规模扰动筛选的计算压缩策略 | **重要** — 极大降低了全基因组 Perturb-seq 的成本 | **Jonathan Weissman** 等 |
| 2024 | AlphaFold3 发表 — 预测蛋白质-蛋白质、蛋白质-配体、蛋白质-核酸复合物结构 | **开创性** — 从单体预测扩展到分子间相互作用；76%预测结构在2埃精度内 | **Demis Hassabis**, **John Jumper** (DeepMind / Isomorphic Labs) |
| 2024 | Evo 发表（Arc Institute）— 长上下文基因组基础模型 | **开创性** — 在数百万原核/噬菌体基因组上训练，跨 DNA/RNA/蛋白质泛化；零样本生成功能性 CRISPR-Cas 系统 | **Patrick Hsu**, Arc Institute |
| 2024 | CRISPR 基因编辑疗法 Casgevy 获 FDA 批准（镰刀细胞病/β-地中海贫血） | **开创性** — 第一个基于 CRISPR 的上市疗法 | Vertex / CRISPR Therapeutics |
| 2024 | **诺贝尔化学奖授予蛋白质结构预测与设计** — David Baker（计算蛋白质设计）、Demis Hassabis 和 John Jumper（AlphaFold 蛋白质结构预测） | **开创性** — AI 驱动的生物信息学方法获最高科学荣誉；标志着计算生物学从"辅助工具"升格为"核心科学方法" | **David Baker**, **Demis Hassabis**, **John Jumper** |
| 2024 | Human Cell Atlas 第一批旗舰图谱发布 — 包括视网膜细胞图谱和类器官图谱 | **重要** — 迈向首个完整的人体细胞图谱草案 | **Aviv Regev**, **Sarah Teichmann**, HCA 联盟 |
| 2024 | Multiome Perturb-seq — 同时测量转录组和表观基因组对扰动的响应 | **重要** — 多组学功能基因组学的融合 | 多个团队 |

---

## 十、2025-2026：前沿动态（最新）

### 2025 年

| 事件 | 影响 | 详情 |
|------|------|------|
| **Evo 2 发布**（Arc Institute, 2025年2月） | **开创性** | 40B 参数的基因组基础模型，在超过128,000个物种的9.3万亿核苷酸上训练；1M碱基上下文窗口；预测 BRCA1 致病突变准确率 >90%；可设计细菌基因组长度的新序列。发表于 Nature。关键学者：**Patrick Hsu** |
| **CZI 与 NVIDIA 联合推进虚拟细胞模型** | **开创性** | 2025年10月宣布合作，目标是将生物数据处理扩展到PB级（数十亿细胞观测），构建下一代细胞模拟模型 |
| **rBio 推理模型发布**（CZI） | **重要** | 在虚拟细胞模型上训练的推理 AI，科学家可用自然语言提问复杂生物学问题（如基因相互作用对细胞状态的影响），在 PerturbQA 基准上超越已有模型 |
| **RAEFISH 全基因组空间转录组学** | **开创性** | 无需测序的全基因组空间转录组方法，可在完整组织中以单分子分辨率对23,000个人类基因进行空间画像。发表于 Cell |
| **Deep-STARmap / Deep-RIBOmap** | **重要** | 在3D厚组织块中同时分析转录和翻译活性，发表于 Nature Methods |
| **SIMO：多组学空间整合** | **重要** | 概率对齐方法整合空间转录组与 scRNA-seq 及其他单细胞模态（染色质可及性、DNA 甲基化等），发表于 Nature Communications |
| **VIPerturb-seq** | **重要** | 全基因组规模 Perturb-seq 平台，通量提升50倍 |
| **Perturb-FISH** | **重要** | 结合空间转录组学与 CRISPR 扰动筛选，发现细胞间和密度依赖的免疫调控，发表于 Cell |
| **Pertpy 框架** | **补充** | Python 端到端扰动分析框架，发表于 Nature Methods |
| **CRISPR 个性化治疗首例** | **开创性** | 首次为单个患者定制体内 CRISPR 治疗方案（婴儿先天性免疫缺陷），从设计到给药仅6个月——首次实现 CRISPR 基因"矫正"（而非简单"破坏"） |
| **CRISPR 降胆固醇一期临床成功** | **重要** | Cleveland Clinic 首个人类临床试验：单次 CRISPR-Cas9 治疗持续降低 LDL 胆固醇和甘油三酯至少60天 |
| **CRISPR 抗癌临床试验** | **重要** | 明尼苏达大学完成首个 CRISPR 基因编辑免疫疗法治疗晚期胃肠道癌的人类临床试验，一名患者达到完全缓解（肿瘤消失2年以上） |
| **基因组语言模型全面综述** | **补充** | 多篇系统性综述（Briefings in Bioinformatics、Frontiers in Genetics）全面梳理了从 DNABERT 到 Evo 2 的基因组语言模型发展轨迹 |
| **HCA 首个完整草案准备中** | **重要** | HCA 2025 大会聚焦第一版人体细胞图谱草案的组装，整合 AI 和空间基因组学技术 |
| **长读长测序精度接近短读长** | **重要** | Oxford Nanopore 目标 Q20-Q30 准确率，结合 PacBio HiFi，长读长在 de novo 组装中发现突变率比短读长多20-40% |

### 2026 年（截至4月）

| 事件 | 影响 | 详情 |
|------|------|------|
| **Human Cell Atlas 首个完整草案即将发布** | **开创性** | 2026年发布首个完整人体细胞图谱草案；2026年6月波士顿大会将聚焦跨组织3D空间参考图谱的构建 |
| **CZI 投资2000万美元用于个性化 CRISPR 治疗** | **重要** | CZI 向 UCSF 和 UC Berkeley 投入2000万美元（3年），用于在8名严重遗传免疫缺陷儿童中测试个性化 CRISPR 治疗 |
| **发育中人脑高分辨率图谱** | **重要** | 约翰霍普金斯大学发布人类发育脑的高分辨率图谱（2026年3月） |
| **Illumina 空间转录组技术即将商业化** | **重要** | 预计2026年商业发布，捕获面积比现有技术大9倍，分辨率提高4倍 |
| **通用生物 AI（GBAI）综述发表** | **重要** | Nature Biotechnology 发表综述，定义了"通用生物人工智能"概念——跨 DNA、RNA、蛋白质和细胞系统的多模态 AI，发表于2026年 |
| **Scribe Therapeutics 表观遗传沉默临床试验** | **补充** | 计划2026年启动靶向 PCSK9 的 CRISPR 表观遗传沉默平台临床试验 |
| **GenomeQA 基准测试** | **补充** | 评估通用 LLM 理解基因组序列能力的基准发布 |
| **全球生物信息学市场规模** | 背景 | 2024年达166.6亿美元，预计2034年超520亿美元 |

---

## 十一、50位核心学者在时间线上的贡献定位

下表汇总本时间线涉及的50位核心学者及其关键贡献时间点：

| # | 学者 | 核心贡献 | 时间节点 | 影响级别 |
|---|------|----------|----------|----------|
| 1 | **Margaret Dayhoff** | 蛋白质序列数据库、PAM矩阵、计算进化 | 1965-1969 | 开创性 |
| 2 | **Frederick Sanger** | 蛋白质测序、DNA测序法、phiX174基因组 | 1955-1977 | 开创性 |
| 3 | **James Watson** | DNA双螺旋、HGP早期领导 | 1953, 1990 | 开创性 |
| 4 | **Francis Crick** | DNA双螺旋、中心法则 | 1953 | 开创性 |
| 5 | **Linus Pauling** | 分子钟假说 | 1962 | 重要 |
| 6 | **Emile Zuckerkandl** | 分子钟假说 | 1962 | 重要 |
| 7 | **Saul Needleman** | 全局序列比对算法 | 1970 | 开创性 |
| 8 | **Christian Wunsch** | 全局序列比对算法 | 1970 | 开创性 |
| 9 | **Temple Smith** | 局部序列比对算法 | 1981 | 开创性 |
| 10 | **Michael Waterman** | 局部序列比对算法、序列分析数学基础 | 1981 | 开创性 |
| 11 | **Kary Mullis** | PCR发明 | 1983 | 开创性 |
| 12 | **David Lipman** | NCBI创建、BLAST算法 | 1988-1990 | 开创性 |
| 13 | **Stephen Altschul** | BLAST算法 | 1990 | 开创性 |
| 14 | **Eugene Myers** | BLAST算法、全基因组鸟枪法组装 | 1990, 1998-2000 | 开创性 |
| 15 | **Webb Miller** | BLAST算法、比较基因组学 | 1990 | 重要 |
| 16 | **William Pearson** | FASTA算法 | 1985 | 重要 |
| 17 | **Amos Bairoch** | SWISS-PROT/UniProt数据库 | 1984 | 重要 |
| 18 | **Sean Eddy** | HMMER、Pfam、profile HMM | 1994-1997 | 重要 |
| 19 | **David Haussler** | HMM引入序列分析、UCSC Genome Browser | 1987, 2001 | 开创性 |
| 20 | **Francis Collins** | 人类基因组计划领导 | 1990-2003 | 开创性 |
| 21 | **Craig Venter** | EST方法、全基因组鸟枪法、Celera人类基因组 | 1991-2001 | 开创性 |
| 22 | **Hamilton Smith** | 限制性内切酶、第一个细菌基因组 | 1995 | 重要 |
| 23 | **Claire Fraser** | 首个自由生活生物基因组 | 1995 | 重要 |
| 24 | **John Sulston** | 线虫基因组、Sanger Centre | 1993-1998 | 开创性 |
| 25 | **Sydney Brenner** | 线虫模式生物、分子生物学基础 | 1998 | 开创性 |
| 26 | **Robert Waterston** | 线虫基因组 | 1998 | 重要 |
| 27 | **Steven Henikoff** | BLOSUM替换矩阵 | 1992 | 重要 |
| 28 | **Ewan Birney** | ENCODE、Ensembl、EBI | 2003-2012 | 开创性 |
| 29 | **David Baker** | 计算蛋白质设计（Top7, Rosetta, RoseTTAFold）、2024诺贝尔奖 | 2003-2024 | 开创性 |
| 30 | **Heng Li** | BWA、SAMtools、minimap2 | 2009-2010 | 开创性 |
| 31 | **Cole Trapnell** | TopHat、Cufflinks、Monocle | 2009-2014 | 重要 |
| 32 | **Ben Langmead** | Bowtie比对工具 | 2008 | 重要 |
| 33 | **Barbara Wold** | RNA-seq方法学 | 2008 | 开创性 |
| 34 | **Wolfgang Huber** | DESeq、Bioconductor统计方法 | 2010 | 重要 |
| 35 | **Jennifer Doudna** | CRISPR-Cas9、2020诺贝尔奖 | 2012, 2020 | 开创性 |
| 36 | **Emmanuelle Charpentier** | CRISPR-Cas9、2020诺贝尔奖 | 2012, 2020 | 开创性 |
| 37 | **Feng Zhang** | CRISPR应用于哺乳动物细胞、CRISPR筛选 | 2012-2015 | 开创性 |
| 38 | **Rickard Sandberg** | Smart-seq单细胞方法 | 2012 | 重要 |
| 39 | **Sten Linnarsson** | 单细胞转录组学先驱 | 2012 | 重要 |
| 40 | **Steven McCarroll** | Drop-seq高通量单细胞 | 2014 | 开创性 |
| 41 | **Aviv Regev** | Human Cell Atlas、Perturb-seq、单细胞分析 | 2014-2024 | 开创性 |
| 42 | **Sarah Teichmann** | Human Cell Atlas联合领导 | 2017-2024 | 开创性 |
| 43 | **Fabian Theis** | Scanpy、单细胞计算方法 | 2017 | 重要 |
| 44 | **Rahul Satija** | Seurat单细胞分析框架 | 2018 | 重要 |
| 45 | **Demis Hassabis** | AlphaFold2/3、2024诺贝尔奖 | 2020-2024 | 开创性 |
| 46 | **John Jumper** | AlphaFold2/3、2024诺贝尔奖 | 2020-2024 | 开创性 |
| 47 | **Alexander Rives** | ESM/ESMFold蛋白质语言模型 | 2021-2022 | 重要 |
| 48 | **Xiaowei Zhuang** | MERFISH空间转录组学 | 2021 | 开创性 |
| 49 | **Karen Miga** | T2T完整人类基因组 | 2022 | 开创性 |
| 50 | **Patrick Hsu** | Evo/Evo2基因组基础模型 | 2024-2025 | 开创性 |

---

## 十二、领域演进的六条主线

回顾60余年历史，生物信息学的演进可归纳为六条相互交织的主线：

### 1. 序列 → 结构 → 功能
- 1960s: 蛋白质序列收集（Dayhoff）
- 1970-80s: 序列比对算法（NW → SW → BLAST）
- 1990-2000s: 基因组测序（HGP）
- 2020s: AI 结构预测（AlphaFold）→ 功能预测（Evo2）

### 2. 批量 → 单细胞 → 空间
- 2000s: 微阵列 → RNA-seq（批量）
- 2012-16: scRNA-seq（单个细胞）
- 2021+: 空间转录组学（原位位置信息）
- 2025+: 全基因组空间转录组（RAEFISH），3D组织分析

### 3. 描述 → 扰动 → 设计
- 观察阶段：测序 → 注释 → 比较
- 扰动阶段：CRISPR筛选 → Perturb-seq → 全基因组扰动图谱
- 设计阶段：计算蛋白质设计（Baker）→ 基因组设计（Evo2）→ 治疗设计

### 4. 单一组学 → 多组学 → 虚拟细胞
- DNA → RNA → 蛋白质（单独分析）
- Multiome: 同时测量多个层次
- 虚拟细胞模型：整合所有层次的数字孪生（CZI/NVIDIA, 2025）

### 5. 专用工具 → 基础模型
- 传统：每个任务一个工具（BLAST、BWA、GATK...）
- 基础模型时代：Evo2（DNA）、ESM（蛋白质）、scGPT（单细胞）— 通用预训练 + 任务微调
- 通用生物AI（GBAI）：跨模态统一模型（2026概念）

### 6. 发现 → 诊断 → 治疗
- 基础研究工具 → 临床基因组学
- 2024: 首个 CRISPR 疗法获批
- 2025: 个性化 CRISPR 治疗、AI 辅助药物发现
- 生信从"科学工具"演变为"临床基础设施"

---

## 参考来源

- [From Protein Structure to Drug Discovery: Bioinformatics Breakthroughs in 2024-2025 (MDPI)](https://www.mdpi.com/1467-3045/48/1/33)
- [AlphaFold Protein Structure Database 2025 (NAR)](https://academic.oup.com/nar/advance-article/doi/10.1093/nar/gkaf1226/8340156)
- [AlphaFold3: Applications and Performance (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC12027460/)
- [Spatial Integration of Multi-Omics with SIMO (Nature Communications)](https://www.nature.com/articles/s41467-025-56523-4)
- [Sequencing-free whole-genome spatial transcriptomics (Cell)](https://www.cell.com/cell/fulltext/S0092-8674(25)01037-2)
- [Large Language Models for Bioinformatics (Wiley)](https://onlinelibrary.wiley.com/doi/full/10.1002/qub2.70014)
- [Comprehensive Survey of Genome Language Models (Briefings in Bioinformatics)](https://academic.oup.com/bib/article/27/1/bbaf724/8426124)
- [Evo 2: DNA Foundation Model (Arc Institute)](https://arcinstitute.org/tools/evo)
- [Genome Modeling with Evo 2 (Nature)](https://www.nature.com/articles/s41586-026-10176-5)
- [Human Cell Atlas to Unified Foundation Model (Nature)](https://www.nature.com/articles/s41586-024-08338-4)
- [Atlas of Cells: Milestone in Understanding the Human Body (CNN)](https://www.cnn.com/2024/11/21/science/atlas-cells-human-biology-body/)
- [T2T Complete Human Genome (Science)](https://www.science.org/doi/10.1126/science.abj6987)
- [Nobel Prize in Chemistry 2024 (NobelPrize.org)](https://www.nobelprize.org/prizes/chemistry/2024/press-release/)
- [CRISPR Clinical Trials 2026 Update (IGI)](https://innovativegenomics.org/news/crispr-clinical-trials-2026/)
- [CZI rBio Reasoning Model](https://chanzuckerberg.com/blog/rbio-reasoning-ai-model/)
- [CZI Virtual Cell Models](https://chanzuckerberg.com/science/technology/virtual-cells/)
- [Generalist Biological AI (Nature Biotechnology)](https://www.nature.com/articles/s41587-026-03064-w)
- [Margaret Dayhoff: Pioneer of Bioinformatics (Nature Computational Science)](https://www.nature.com/articles/s43588-025-00784-y)
- [VIPerturb-seq for Genome-Wide Screens (bioRxiv)](https://www.biorxiv.org/content/10.64898/2026.02.12.705613v1.full)
- [Perturb-FISH: Spatial CRISPR Screening (Cell)](https://www.cell.com/cell/fulltext/S0092-8674(25)00197-7)
- [Pertpy Framework (Nature Methods)](https://www.nature.com/articles/s41592-025-02909-7)
- [Illumina Spatial Transcriptomics](https://www.illumina.com/company/news-center/press-releases/2025/10a7ec49-da37-40d8-8aff-0e8e149b9534.html)
- [High-Resolution Atlas of Developing Human Brain (JHU)](https://hub.jhu.edu/2026/03/26/high-resolution-atlas-developing-human-brain/)
