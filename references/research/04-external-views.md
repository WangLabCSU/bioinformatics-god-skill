# 04 - External Perspectives, Criticisms & Reflections on Bioinformatics

> Collected 2026-04-10. Sources from peer-reviewed literature, prominent blogs, and community discussions.

---

## 1. Criticisms of Bioinformatics

### 1.1 The Reproducibility Crisis

Bioinformatics faces a severe reproducibility problem. A 2009 systematic evaluation found only 2 of 18 published articles could be reproduced (11%). In systems biology modeling, roughly 49% of models could not be reproduced from published manuscripts alone.

**Root causes identified:**
- Incomplete or erroneous descriptions of simulations (software versions, parameters)
- Missing code, missing essential methodology steps
- Changes in reference data formats over time
- Lack of version-controlled compute environments

**Proposed framework -- the "Five Pillars of Computational Reproducibility":**
1. Literate programming
2. Code version control and sharing
3. Compute environment control (containers, etc.)
4. Persistent data sharing
5. Comprehensive documentation

> Key refs: Sandve et al., PLOS Comput Biol (2013); Schwab et al., GigaScience (2018); Kim et al., Briefings in Bioinformatics (2023); Tiwari & Tiwari, Genome Biology (2024).

### 1.2 P-value Abuse and Statistical Methodology

The misuse of p-values has become a major concern in genomics, especially with high-dimensional data.

**Core problems:**
- Inflated Type I errors from massive multiple testing without proper correction
- Researchers treating arbitrary p < 0.05 thresholds as biological truth
- The GWAS p-value threshold of 5x10^-8 is a pragmatic convention, not a biological constant
- The American Statistical Association (ASA) has issued formal warnings against p-value misuse

**Alternatives gaining traction:** False discovery rate (FDR) control, Bayesian approaches, effect size reporting, confidence intervals, and pre-registration of analysis plans.

### 1.3 Wet Lab Biologists' View: "Just Computational"

A persistent cultural tension exists between experimental and computational biologists:

- Bioinformaticians are often perceived as providing a "service" or "support" function
- Cross-cultural working arrangements between computational and wet lab researchers are sometimes a greater source of tension than pure method development
- Bioinformaticians are frequently middle authors, making career advancement difficult

### 1.4 "Tool Paper" Culture

- **Incentive misalignment:** Bioinformatics programs are 31-fold over-represented among the highest-impact scientific papers, but this reflects citation counts for tools (BLAST, BWA, GATK), not biological discoveries
- **"A Farewell to Bioinformatics" (Fred Ross, 2012):** A viral rant arguing the field produces poor software to extract science from poor experimental results

### 1.5 Unfair Benchmarking

Most papers introducing new methods claim superior performance, but independent "neutral" benchmark studies often fail to replicate these claims.

**Systematic biases:** Selection of favorable datasets, better ability to fix bugs in one's own method, selective reporting of method variants that perform best.

---

## 2. Disciplinary Self-Reflection

### 2.1 Lior Pachter's Methodological Critiques

- **Software quality:** "Most bioinformatics software is of very poor quality."
- **Statistical errors:** Publicly identified false positives in memory-related gene expression studies
- **"Network nonsense papers":** Systematic critique of poorly conceived network biology analyses

### 2.2 Is Bioinformatics a Discipline?

The field suffers from a persistent identity crisis:
- Bioinformaticians as producers of "secondary inscriptions" are institutionally subordinate to biologists
- Computer science and biology have fundamentally different cultures, values, and products
- The field exists in "middleness" -- branded as a conduit rather than a destination

### 2.3 Education and Training Gaps

Despite 20+ years of calls for action, the bioinformatics skills gap has not narrowed -- and may be widening.

### 2.4 Data Sharing and Open Science

FAIR principles under revision. A 2021 Nature investigation found that despite policies requiring data sharing, compliance is inconsistent and enforcement is weak.

---

## 3. Technical Paradigm Shifts -- External Evaluations

### 3.1 Statisticians on Deep Learning in Genomics

- **Black box problem:** Models make decisions that cannot be explained to end users
- **Overfitting risk:** High-dimensional omics data with limited sample sizes is a perfect storm
- **Philosophical divergence:** ML optimizes prediction; statistical inference seeks to understand causal processes

### 3.2 AlphaFold -- Multi-Perspective Assessment

**Genuine achievements:** Accelerated experimental structural biology workflows, made structural biology accessible to non-specialists.

**Critical limitations:** Cannot model protein dynamics, ~1/3 of residues potentially lack atomistic precision, cannot predict effects of mutations on structure and stability.

### 3.3 Single-Cell Technologies -- Sober Assessment

- Captures only 10-40% of total RNAs per cell
- Spatial context is inherently lost during tissue dissociation
- Pseudoreplication is rampant in differential expression analyses

### 3.4 Large Language Models in Biology

- Medium-sized models often perform as well as 20x larger variants
- Data leakage from pretraining inflates prediction scores
- Synthetic sequences from gLMs fail to preserve long-range genomic organization

---

## 4. Cross-Disciplinary Perspectives

### 4.1 Computer Scientists: Bioinformatics has not benefited from decades of software engineering advances
### 4.2 Clinicians: Few healthcare organizations offer precision medicine as routine clinical workflow
### 4.3 Pharma: Academic bioinformatics tools often lack the robustness and scalability required for industrial pipelines

---

## 5. Synthesis: Recurring Themes

| Theme | Core message |
|-------|-------------|
| **Reproducibility** | The field cannot reliably reproduce its own results |
| **Software quality** | Scientific code is held to lower standards than any other software domain |
| **Biological relevance** | Computational results frequently lack biological validation |
| **Statistical rigor** | P-value abuse, benchmark gaming, and pseudoreplication are endemic |
| **Translation gap** | Academic results rarely survive contact with clinical/industrial reality |
| **Cultural silos** | Bioinformatics lives between disciplines and is valued by none fully |
| **Hype cycles** | Each new technology follows the same overpromise-underdeliver cycle |
| **Incentive misalignment** | Reward structures favor novel tools over robust, validated work |
