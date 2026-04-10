# 生物信息学顶级学者：对话、辩论与思维模式

## 一、经典辩论与争议

### 1.1 Lior Pachter vs Manolis Kellis：方法论诚信之争

**背景**：2014年，UC Berkeley（现Caltech）数学家/计算生物学家 Lior Pachter 在其博客 "Bits of DNA" (liorpachter.wordpress.com) 发表系列文章，公开指控 MIT 教授 Manolis Kellis 的 Network Deconvolution 论文（Feizi et al. 2013, Nature Biotechnology）存在欺诈行为。

**Pachter 一方的核心指控**：
- 论文中描述的方法与实际产生结果的方法不同——"方法用来获得结果的与主文本中的完全不同"
- 作者在论文发表后悄悄替换了关键补充图表，未通知编辑或发表更正
- 方法中存在隐藏参数，作者"试图隐藏方法中参数的存在"
- 独立复现失败——Pachter 甚至公开悬赏给任何能精确复现论文图表的人

**Kellis 一方的回应**（Feizi, Marbach, Medard, Kellis 联合声明，compbio.mit.edu）：
- Pachter 的欺诈指控"毫无根据且错误"——"fraud 在科学界有非常特定的含义，涉及伪造、篡改或抄袭，这些都与此无关"
- 指责 Pachter "煽动性和个人化的指控极具反效果，质疑作者诚信和煽动性言辞偏离了有意义的科学辩论"
- 声称独立实现者已成功验证了方法
- 指出 Pachter 的技术评论曾被 Nature Biotechnology 同行评审后拒绝发表

**Pachter 的思维模式（关键洞察）**：
- **不预设善意**："通常读论文读不通时，我会假设是自己的问题。但现在，当 Feizi et al. 的论文开始讲不通时，我不再假设问题出在我身上。" 这是一种从信任到验证的认识论转变。
- **系统性批判**：不仅批评单篇论文，而是追踪一个作者的整体行为模式——"Manolis Kellis 不是普通科学家。他在 ENCODE、mod-ENCODE 等主要联盟项目中扮演领导角色。"
- **方法论纯洁主义**："计算生物学中，向数学恐惧的生物学家兜售不连贯的数学并不困难。"
- **2019年五年后回顾**：Pachter 追踪后续独立验证（Wang et al. 2018），确认 Network Deconvolution 表现不佳，总结出"胡说方法倾向于产生胡说结果"（Nonsense methods tend to produce nonsense results）。

**更广泛的影响**：这场辩论触及了科学界的核心问题——博客批评 vs 正式同行评审的合法性。Pachter 后来倡导建立"Journal of Scientific Integrity"（科学诚信期刊），专门用于系统性地批评某位作者的多篇有问题的工作。

> 来源：liorpachter.wordpress.com/2014/02/11/the-network-nonsense-of-manolis-kellis/; liorpachter.wordpress.com/2014/02/12/why-i-read-the-network-nonsense-papers/; compbio.mit.edu/nd/Response_to_Nonsense_Blog_Post.pdf; liorpachter.wordpress.com/2019/02/11/nonsense-methods-tend-to-produce-nonsense-results/

---

### 1.2 Pachter vs Salmon/Patro：RNA-Seq 量化方法之争

**背景**：2017年，Pachter 在博客发表 "How not to perform a differential expression analysis"，质疑 Rob Patro 的 Salmon 工具本质上是 kallisto 的重新实现，以及其 GC 偏差校正的实际效果。

**Pachter 一方**：
- Salmon 直接实现了 kallisto 的伪比对核心思想，两者输出极其相似
- GC 偏差校正的实际效果被论文夸大——在典型差异表达实验中效果有限
- 用单个样本（ERR188140）定量证明两个工具的输出"非常非常强的相似性"

**Patro 一方**（联合 Michael Love, Rafael Irizarry, Carl Kingsford）：
- 指责 Pachter 选择了单一样本，可能存在樱桃采摘
- 坚持 GC 偏差校正"显著提高了丰度估计的准确性和后续差异表达分析的灵敏度"
- 在推荐工作流（Salmon + tximport + DESeq2）下效果差异缩小到 32%

**思维模式洞察**：Pachter 对此的逐点反驳展现了一种"定量诚实"的思维——他认为从 353% 差异缩小到 32% 并不是"结果仍然相似"，而是承认了显著的初始差异。这反映了一种对数字敏感、不容许修辞性模糊的思维方式。

> 来源：liorpachter.wordpress.com/2017/09/（September 2017 archive）

---

### 1.3 Seurat vs Scanpy：单细胞分析生态系统之争

**背景**：Seurat（R, Satija Lab, 2015）和 Scanpy（Python, Theis Lab, 2017）是单细胞 RNA-seq 分析的两大主流平台，长期被认为实现了相似的标准流程。

**Pachter 实验室的系统性比较**（Rich et al. 2024, bioRxiv）揭示了令人不安的差异：
- Seurat 和 Scanpy 在默认参数下产生"相当大的差异"
- 差异程度相当于"测序少于 5% 的 reads 或分析少于 20% 的细胞群体"所引入的变异
- 不同版本的同一工具（如 Seurat v5 vs v4）也可能产生显著不同的结果
- 高变基因选择、聚类、差异表达分析等关键步骤存在未文档化的差异

**具体技术差异**：
- Scanpy 的 `highly_variable_genes(flavor='seurat')` 与 Seurat 的实际 HVG 结果差异巨大——500个基因中仅138个重叠（GitHub Issue #2780）
- 两个工具的默认方法实际上是不同的方法——造成广泛困惑
- Scanpy 默认排名方式导致"数学上不正确的基因排名"（Pullin et al. 2024, Genome Research）

**核心争议不是哪个更好，而是**：
- "生物信息学数据分析中一个典型的隐含假设是，包之间的选择和版本对结果解释的影响应该很小或没有。然而，已经观察到包或版本之间存在相当大的变异性。"
- 这实质上是一个**可重复性问题**——两个"相同"分析可能给出不同的生物学结论

**社区态度**：
- R vs Python 的选择往往基于编程习惯而非科学理由
- 大多数用户不了解底层实现的差异
- Scanpy 社区（scverse）积极修复与 Seurat 的不一致性（如 `seurat_v3_paper` flavor）

> 来源：biorxiv.org/content/10.1101/2024.04.04.588111; github.com/scverse/scanpy/issues/2780; link.springer.com/content/pdf/10.1186/s13059-024-03183-0.pdf

---

### 1.4 AlphaFold 对结构生物学的冲击

**"蛋白质折叠问题已解决"——但辩论继续**

**激进一方**：
- CASP14 组织者认可 AlphaFold2 作为"50年蛋白质折叠问题的解决方案"
- Ourmazd et al. 2022 文章标题"Structural biology is solved -- now what?"
- DeepMind 官方："几乎所有已编目的蛋白质"的结构已被预测（2亿+）
- 诺贝尔委员会2024年授予化学奖

**审慎/反对一方**：
- **Moore et al. 2022 (Science)**："蛋白质折叠问题：尚未解决"——"目前最好的情况下，预测精度不优于约4 Angstrom 分辨率"，且真正解决需要"基于底层物理和化学的基本原理"
- **Tom Terwilliger 团队**（2024, Nature Methods）：系统评估发现"最高置信度的 AlphaFold 预测的误差约为高质量实验结构的两倍"，且"约10%的最高置信度预测存在非常实质性的误差"
- **IUCr Newsletter 评论者 John Helliwell**：坚持预测必须用实验验证，对功能状态的多构象预测能力存疑
- **Alexandre de Brevern** (2024)：警告"AlphaFold 误用的第二波"——非专家将预测当作实验确定的结构

**John Jumper（AlphaFold 核心开发者）的自我评估**（2025, MIT Technology Review）：
- "这并不意味着我们对其中所有内容都确定。这是一个预测数据库，它带有预测的所有注意事项。"
- "我对科学家们使用它的方式感到震惊——在解释它和在实践中使用它方面，大约如它应该被信任的那样，既不太多也不太少。"

**Kliment Verba（UCSF，AlphaFold 长期用户）的务实评估**：
- "这是一项令人难以置信的有用技术，毫无疑问。我们每天都在使用它。"
- "但有很多情况下你得到一个预测，你不得不挠头——这是真实的还是不是？不完全清楚——有点borderline。"
- "它有点像 ChatGPT——它会以同样的自信对你胡说八道。"
- "它并没有真正替代任何实验，但它相当程度地增强了它们。"

**AlphaFold3 的开源争议**（2024, Nature Editorial）：
- AlphaFold2 开放了完整代码；AlphaFold3 只提供伪代码
- Nature 发表了公开信批评这限制了验证和可重复性
- DeepMind 承诺在六个月内发布学术用途模型权重
- Nature 编辑辩护：需要与私营部门合作，但承认争议合理

**Isomorphic Labs 的"AlphaFold 4"**（2026年2月，Nature News）：
- DeepMind 药物开发子公司推出更强大的模型，但完全不公开
- 标志着从开放科学到商业封闭的进一步转向

> 来源：nature.com/articles/d41586-026-00365-7; iucr.org/news/newsletter/volume-30/number-1/; nature.com/articles/d41586-024-01463-0; technologyreview.com/2025/11/24/1128322/; biosciences.lbl.gov/2024/01/23/; nature.com/articles/d41586-025-00111-5; mdpi.com/2673-7426/4/4/124/pdf

---

### 1.5 开源 vs 商业化：Broad Institute GATK 的曲折历程

**背景**：GATK（Genome Analysis Toolkit）是变异发现的行业标准工具，由 Broad Institute 开发。其授权模式经历了多次争议性变化。

**GATK 授权时间线**：
1. **早期（GATK 1.x）**：MIT 开源许可证
2. **GATK 2.0（2012）**：部分代码闭源，"GATK-Lite"提供基础功能但缺少前沿工具；商业使用需通过 Appistry 获取许可
3. **社区反弹**：被批评为"不是开源"——"这种'仅学术用途开源'的胡说八道太普遍了"（社区评论）；部分开发者指出 BSD-3 条款的误导性宣传
4. **GATK 3.x**：恢复源代码可见性，但保留学术非商业限制
5. **2017年决定全面开源**（Anthony Philippakis, Broad CDO）：
   - "在仔细评估实验后，我们得出结论，是时候做出改变了"
   - 三个原因：(a) 技术支持需要比商业合作伙伴更多的专业知识；(b) 许可限制了社区修改和共享代码的能力；(c) 云部署减轻了本地安装的负担
6. **GATK4（2018）**：Apache 2.0 开源许可，允许商业使用

**Eric Lander 的开放科学哲学**：
- "Lander 是确保大规模基因组信息和工具自由和即时可用的先驱——从其实验室的小鼠遗传图谱开始，延续到人类基因组计划对免费数据共享的承诺。"
- 人类基因组计划的核心原则：数据"自由且无限制地发布"——与 Celera Genomics 的专有策略形成鲜明对比

**Lander 关于公共 vs 私有竞争的思考**（CSHL Oral History）：
- "整个人类基因组计划作为'大科学'的概念是有些误导的。它基于对物理学的类比……但人类基因组计划不是那样的。它是关于使小科学高效的基础设施。"
- Lander 积极推动公共资助科学家加速工作，在 Celera 之前将基因组片段发布到公共域

> 来源：broadinstitute.org/blog/open-source-foundation-future; gatk.broadinstitute.org; github.com/broadinstitute/gatk; sites.google.com/a/broadinstitute.org/legacy-gatk-documentation/announcements/; dnalc.cshl.edu/view/15319/; library.cshl.edu/oralhistory/speaker/eric-lander/

---

## 二、关键演讲与访谈中的思维模式

### 2.1 Eric Lander：数学家转基因组学家的框架思维

**核心思维模式**：

1. **基础设施思维**："人类基因组计划被设计为小科学的使能者，这就是它成功的原因。"不是做一个大实验，而是建设让所有人都能用的基础设施。

2. **经济泵动原理**（PNAS 2011 QnA）："在1950年代，国防部向工业界发出信号，它将成为计算机的主要客户。这推动了价格下降。在1990年代，人类基因组计划产生了类似效果。" Lander 用经济学思维理解技术推动。

3. **耐心的现实主义**（STAT, 2016）："大多数癌症治愈将需要数十年"——反对过度承诺。"理解疾病相关的细胞通路是许多药物开发努力的基础"——强调路径理解先于治疗。

4. **目标分层**："研究与常见病相关的基因有两个不同目标。首要目标是理解疾病背后的生物学通路。"将基础理解置于直接应用之上。

**争议面**：
- 2018年为 James Watson 90岁生日举杯——在 Watson 种族言论争议后引发批评
- 2022年因对待下属问题离开白宫科技政策办公室

> 来源：ncbi.nlm.nih.gov/pmc/articles/PMC3136317/; broadinstitute.org/directors-page; dnalc.cshl.edu/view/15319/; en.wikipedia.org/wiki/Eric_Lander

---

### 2.2 David Baker：蛋白质设计的"疯子边缘"

**TED 2019 演讲核心**："5 challenges we could solve by designing new proteins"——将蛋白质设计框架化为"我们的新超能力"。Baker 不仅展示科学，而是用挑战-解决方案的叙事结构传递愿景。

**诺贝尔奖演讲（2024年12月）**："De Novo Protein Design"

**Baker 的思维模式**：

1. **从理论到可验证的实物**：Top7（2003）的突破性在于不仅是计算设计，而是实验验证了一个自然界不存在的蛋白质折叠。"这是一个真正了不起的成就"（诺贝尔委员会语）。

2. **平台思维**：Rosetta 不是一个工具，而是一个生态系统——"一个社区用户和共同开发者的干部"。Baker 培养了超过90位（现100+）独立教职人员。

3. **"疯子边缘"的自我定位**：在2024年诺贝尔新闻发布会上，Baker 提到他的工作"仍然可以被称为疯子边缘"（Lunatic Fringe）。这种自嘲式的定位反映了一种将不可能视为尚未解决的思维。

4. **从还原到工程**："我们已经进入一个时代，我们不仅能理解生物系统，还能创造新的。"

5. **AI 的整合态度**：Baker 实验室近年积极采用机器学习（RFdiffusion 等），但将其视为增强而非替代计算物理方法。

**2025年6月 TED Membership 对话**：
- "蛋白质是携带出我们身体和所有生物体中所有重要工作的微型机器"
- "我认为我们真的才刚开始"——始终保持'开始'的认知框架

> 来源：ted.com/talks/david_baker_5_challenges; nobelprize.org/prizes/chemistry/2024/baker/lecture/; ipd.uw.edu/2024/10/david-baker-wins-nobel-prize/; youtube.com/watch?v=g96tXNwrYXc

---

### 2.3 Aviv Regev：从单细胞到数字生物学的系统愿景

**核心叙事**：Regev 的思维可以用一个 Marcel Proust 引语框架化——"真正的发现之旅不在于寻找新大陆，而在于用新的眼睛看"。她在 Eric Topol 的 Ground Truths 播客（2024）中即兴引用了这句话（虽然自称"完全搞砸了引用"）。

**思维模式**：

1. **从量变到质变**（a16z "When Quantity Becomes Quality" 播客, 2023）：
   - 当单细胞测序达到足够规模时，量的变化产生了质的飞跃——从描述到理解
   - 这不仅是技术进步，而是认识论的转变

2. **2012年是关键年份**（Topol 访谈, 2024）：
   - "2012年是一个非凡的年份——CRISPR 和单细胞分析同年出现"
   - Regev 看到的不是两个独立技术，而是它们汇聚的可能性

3. **人类作为模式生物**（Nature Reviews Drug Discovery, 2021）：
   - "人类正在成为模式生物"——高分辨率单细胞技术使直接研究人类生物学成为可能
   - "作为社区，我们在研究人类生物学方面一直受限，尤其是高分辨率方面。过去十年发生了巨大变化。"

4. **从好奇到行动的转变**：
   - Regev 从 Broad Institute 转到 Genentech 领导研发："作为科学家，我们在报告和论文中说为什么做这些事、它们最终将如何帮助理解生物学和疾病。我实际上相信这些话，不只是说说。"
   - 这代表了一种**言行一致的知识分子诚信**

5. **规模化的组织智慧**：
   - Human Cell Atlas：从2016年93位科学家的启动会议发展到2700+成员、86个国家
   - "37.2万亿个细胞"——始终用具体数字锚定愿景的规模
   - 合作而非竞争："Aviv 知道做伟大科学部分取决于培养一群合作而非竞争的人"（Anthony Philippakis, GV）

**在 NPR（2025年4月）的公众叙事**：
- "人类基因组计划中，我们只需要处理一个基因组。但记住，一个基因组产生许多许多不同类型的细胞。"
- "某些数字比宇宙中原子的数量还大，所以很大。"——用具体对比让公众理解规模

> 来源：erictopol.substack.com/p/aviv-regev-the-revolution-in-digital; a16z.com/podcast/when-quantity-becomes-quality-with-aviv-regev; nature.com/articles/d41573-021-00051-5; gv.com/news/theory-and-practice-podcast-aviv-regev; npr.org/transcripts/g-s1-60986

---

### 2.4 Rob Knight：微生物组研究的民主化思维

**TED 2014 核心信息**：
- "你随身携带的三磅微生物可能比你基因组中每一个基因都更重要"
- 用90%的准确率从微生物DNA判断肥胖，但只能用58%的准确率从人类DNA判断——用具体对比颠覆直觉

**思维模式**：

1. **公民科学先锋**：American Gut Project 让超过10,000普通人邮寄粪便样本参与研究——"让人们在这个微生物地图上标记自己的位置"
2. **GPS 隐喻**："我们需要开发一个微生物GPS——不仅告诉你在地图上的位置，还告诉你想去哪里以及如何到达"
3. **跨学科思维**：儿科学 + 计算机科学双重任命——"这本身就是一个21世纪的学术头衔"
4. **个体化 vs 群体化**："文献中的一切都基于群体平均值。我们对人了解的一件事是每个人都不同。"

> 来源：ted.com/speakers/rob_knight; knightlab.ucsd.edu/?p=313; thequantifiedbody.net/human-microbiome-health-dr-rob-knight/; extendedstudies.ucsd.edu/news-events/extended-studies-blog/50-voices-of-the-future-rob-knight

---

### 2.5 Eugene Koonin：演化思维的极致纯粹

**核心自我定位**：
- "科学不仅仅是工作甚至职业——它是我体验世界的本质方式。它实际上是对创造性但理性思维的奉献。这些东西可以适用于世界上的一切。"
- "我根本没有好的方式来思考另一种存在模式。"

**思维模式**：

1. **100%计算，0%实验**："我实验室100%的研究是计算性的，不一定是建模，但100%是由计算机完成的，0%是实验完成的。当然，我们持续与实验实验室合作。"

2. **关于自然选择的精确措辞**：
   - "主流科学界现在没有人从字面上理解选择。"（2017年访谈）
   - "现代综合论已经消失了"（2009年论文）——但他澄清这不是戏剧性的立场转变
   - 他的精确性在于：群体遗传学是一个数学框架；自然选择是隐喻性的——但在主流思维中"没有混淆"

3. **从病毒到生命起源的推理链**：
   - CRISPR-Cas 系统的早期识别者（2002年，与 Kira Makarova 合作）
   - 重建真核生物最后共同祖先（LECA）的病毒组——发现"真核生物所有病毒都从感染细菌的病毒进化而来。这是出乎意料的。"
   - 从膜的差异推导出为什么古菌病毒消失——"古菌病毒无法穿透细菌膜"

4. **物理学-生物学的桥接**：
   - "当你研究生命时，你无法逃避物理学的原理"
   - 与物理学家合作，用统计物理原理构建一般演化理论
   - 著作《The Logic of Chance》（机会的逻辑）——标题本身就体现了将确定性和随机性统一的思维

> 来源：ncbi.nlm.nih.gov/pmc/articles/PMC5293061/; oscillations.net/2021/02/21/encore-eugene-koonin/; nlmdirector.nlm.nih.gov/2023/06/07/; findinggeniuspodcast.com/podcasts/understanding-our-era-of-biological-evolution/; en.wikipedia.org/wiki/Eugene_Koonin

---

## 三、AI/深度学习进入生物信息学的态度光谱

### 3.1 热情拥抱者

**David Baker**：将 AI 视为蛋白质设计的加速器。从 Rosetta（物理+计算）到 RFdiffusion（深度学习），Baker 实验室展示了 AI 如何增强而非替代领域知识。

**Aviv Regev**："数字生物学的革命"——引用 Jensen Huang（NVIDIA）："下一个惊人的革命将来自数字生物学。有史以来第一次，生物学有机会成为工程，而不仅仅是科学。" Regev 将 AI 视为从观察到设计的转变工具。

### 3.2 务实使用者

**John Jumper**（AlphaFold）：对自己工具保持谦逊——"这是一个预测数据库，带有预测的所有注意事项。"

**Kliment Verba**（UCSF）：每天使用 AlphaFold 但清楚其局限——"它有点像 ChatGPT——会以同样的自信对你胡说八道。"

### 3.3 深度怀疑者

**Steven Salzberg**（2026年3月博客）："AI 迫切需要一剂怀疑主义"：
- "声称仅凭 DNA 序列就能预测基因行为在生物学上是不可信的"
- 批评 AI 科学家"从工具出发寻找问题"——"这不是好科学的做法。你不是先有工具再找问题。"
- "这些声称在很大程度上是不可证伪的"——触及波普尔科学哲学
- 但也承认"AlphaFold 解决了50年的蛋白质折叠问题"等真正突破

**Nature Genetics (2023)**："当前基因组深度学习方法难以充分捕获人类遗传变异"——系统性发现 Enformer 等模型在预测个体特异性基因表达方面表现不佳

**从怀疑到拥抱的转变案例**（Albi Celaj, Deep Genomics, 2025）：
- 2014年："我记得那种乐观，但认为这些努力不可能涉及湿实验室的现实"
- 转折点：Keras 让他"几分钟内"解决了之前用传统方法无法解决的问题
- "回到2014年的会议室，我不确定如何看待 AI 乐观主义。今天，我会告诉年轻时的自己..."
- 但仍保持警惕："一个好的锤子让你去找钉子"

> 来源：stevensalzberg.substack.com/p/ai-is-starting-to-look-like-pseudoscience; nature.com/articles/s41588-023-01517-5; deepgenomics.com/blog/skeptic-builder-why-i-changed-my-mind-about-ai-biology/

---

## 四、P-Hacking 与统计滥用的跨领域辩论

### 4.1 Ioannidis 的"大多数发表的研究发现是假的"

John Ioannidis 2005年论文 "Why Most Published Research Findings Are False" 是最被引用的论文之一。其核心论点：在现实的效应大小普遍性和研究设计假设下，发表的 p < 0.05 结果的阳性预测值经常低于50%。

### 4.2 生物信息学中的特殊问题

**高通量测序差异表达分析的全领域评估**（Pall et al. 2023, PLOS Biology）：
- 仅 25% 的实验产生了理论预期的 p 值直方图形状
- 37% 的实验 pi0 < 0.5——"好像大多数基因都改变了表达水平"
- 结论："差异表达分析领域存在普遍偏差"

### 4.3 Pachter vs Quake/Sudhof（2025年，Nature Matters Arising）

一个鲜活的案例：Stanford 的 Stephen Quake 和 Thomas Sudhof 在 2024 Nature 论文中未使用 Benjamini-Hochberg 多重比较校正。

**批评方**（Eran Mukamel, Lior Pachter 等）：
- 测试3,350个基因时，p=0.05 预期产生约160个假阳性
- 将单细胞视为独立样本忽略了个体间差异——"统计分析忽略了样本内依赖性，导致过度自信的结果"
- 存在"双重浸泡"（double-dipping）——限制分析为"生物学有意义的调控"的基因

**作者辩护**：采用"更宽松的方法"以避免"因过于严格而忽略真正效应"

**Timothy O'Leary（旁观者评论）**：
- "基于不保守的统计分析来否定所有结果是不公平的"
- "采取保守方法并不保证好科学"
- 这反映了探索性（发现驱动）vs 确认性（假设驱动）研究的根本张力

> 来源：thetransmitter.org/statistics/memory-study-sparks-debate-over-statistical-methods; journals.plos.org/plosbiology/article/file?id=10.1371/journal.pbio.3002007; americanscientist.org/article/the-statistical-crisis-in-science

---

## 五、改变立场的关键时刻

### 5.1 Broad Institute GATK 开源转向（2017）
从部分闭源商业许可回到全面开源——Anthony Philippakis："仔细评估实验后，我们得出结论是时候做出改变了。"社区反馈直接驱动了决策转向。

### 5.2 AlphaFold 从开放到封闭的渐变（2021-2026）
- AlphaFold2（2021）：完全开源代码+200M结构数据库
- AlphaFold3（2024）：仅伪代码，引发公开信批评
- "AlphaFold 4" via Isomorphic Labs（2026）：完全专有
- 这个转变折射出基础研究 vs 商业化的根本张力

### 5.3 Eugene Koonin 的"非转变"
Koonin 在2009年写道"直言不讳地说，现代综合论已经消失了"，后来在2017年澄清："我的思想并没有太大变化。坦率地说，如果我重写的话..."——这是一个学者坚持核心立场但改进表达方式的例子，而非真正的立场转变。

### 5.4 从怀疑者到构建者的AI态度转变
Albi Celaj 的十年历程代表了许多计算生物学家的轨迹：从2014年的"不可能"到2025年的"我们才刚刚开始"，关键转折不是理论说服，而是动手体验（"Keras 让它几分钟内就工作了"）。

---

## 六、思维模式总结：顶级学者的共性与差异

### 6.1 共性

1. **定量诚实**：无论是 Pachter 对数字差异的追究、Baker 对实验验证的坚持、还是 Koonin 对措辞的精确性，顶级学者都对数字和语言保持高度敏感。

2. **长期视角**：Lander 的"癌症治愈需要数十年"、Regev 的37万亿细胞图谱、Baker 的"我们才刚开始"——都拒绝短期炒作。

3. **基础设施优先于应用**：HGP 是"小科学的使能者"、Human Cell Atlas 是"图谱先于治疗"、GATK 是"工具先于发现"。

4. **在确定性和不确定性之间精确导航**：Jumper 的"预测的所有注意事项"、Terwilliger 的"异常有用的假说"——承认成就但标注边界。

### 6.2 差异

| 维度 | 激进批评型（Pachter, Salzberg） | 建设愿景型（Regev, Lander） | 纯粹探索型（Koonin, Baker） |
|------|------|------|------|
| 对错误的反应 | 公开指控，追究到底 | 引导社区规范 | 视为科学进程的一部分 |
| 博客/公开表态 | 高频率、尖锐 | 战略性、面向未来 | 专注学术出版 |
| 对AI的态度 | 怀疑、要求证据 | 拥抱、整合到愿景 | 务实工具主义 |
| 核心驱动力 | 方法论正确性 | 疾病理解/治疗 | 基本原理/真理 |

### 6.3 即兴回答中展现的思维

- **Pachter** 在辩论中的即兴反应往往是精确的数字反驳——"从353%差异缩小到32%不是'结果仍然相似'"
- **Regev** 即兴引用 Proust——然后自嘲"完全搞砸了引用"，展现了文学-科学交融的思维方式
- **Koonin** 被问到争议时的反应："科学丑闻和争议是无效的。他更喜欢实验室而非公众场合。"但他对精确措辞的坚持暴露了深层的认识论关切
- **Baker** 在诺贝尔新闻发布会上的"疯子边缘"自嘲——将不可能正常化为尚未实现
- **Knight** 用大便邮寄的幽默打破公众对微生物组研究的距离感——"让人们对'他们的便便里有什么'感到好奇"
