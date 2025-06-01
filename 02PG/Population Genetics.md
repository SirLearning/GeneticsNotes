注重数理细节的框架，来理解自然群体的进化过程。
- 所以其实他们也并不理解进化和遗传的分界线。都是研究一个方向的事物

群体遗传对下面这些过程进行建模：
- 选择过程
- 遗传漂变
- 突变
- 迁移

# Basic population genetics

## 概率论

[[Probability]]

## 哈代-温伯格原理

基本定义
- IBD，IBS
- 基因型
- allele frequency

Wright-Fisher model

Hardy-Weinberg Principle：平衡状态
- 无论当前基因型如何，群体经过一次随机交配后，会达到该平衡状态。
- 可以通过卡方检验来检验该平衡

## 遗传漂变

遗传漂变 (genetic drift)
- Buri experiment
- 杂合子 (heterozygosity) 的衰减

突变和漂变 (mutation and drift)

## 迁移与群体结构

自交 (inbreeding)
- 基因型频率
- 自交系数 (inbreeding coefficient)

迁移和群体分化 (Migration and population divergence)
- 小岛模型
- Fst 随着迁移数量的变化

Wahlund's principle

## 溯祖理论

溯祖理论 (the coalescent)
- 基因谱：genealogy, lineage
- Wight-Fisher 群体模型
- 溯祖过程
	- 几何分布与指数分布
	- 两条序列的溯祖过程
	- 多条序列的溯祖过程
- 树的高度 (the height of trees, TMRCA)
- 总枝长 (total branch length)

## 分子群体遗传学与统计推断

遗传多态性：即突变
1. ​点突变/单核苷酸多态（Single Nucleotide Polymorphism, SNP）​
    - ​定义：单个碱基对的替换
	    - 转换（transition，嘌呤↔嘌呤或嘧啶↔嘧啶）​
	    - 颠换（transversion，嘌呤↔嘧啶）​
    - ​速率：
        - 人类：约每代每碱基 $1.2 \times 10^{-8}$（约每代每个体60个新点突变）。
        - 果蝇：速率更高，约 $3.5 \times 10^{-9}$ 每碱基每代。
    - ​特殊类型：
        - ​成簇SNP（cSNP）​：由DNA修复错误导致，一次事件引发多个邻近位点突变。
2. 单倍型 (haplotype): 
	- combination
	- linkage disequilibrium (LD)
	- 多位点单倍型结构
	- 等位基因频谱 (allele frequency spectrum, site frequency spectrum, sample frequency spectrum)
	- 联合等位基因频谱 (joint allele frequency spectrum)
	- Maximum Likelihood Inference
		- likelihood function
		- find the $\theta$ that maxmum the $L(\theta)$
3. 微卫星/短串联重复序列 (STR)
4. 限制性片段长度多态 (RFLP)​
5. 插入/缺失（Indels）​
    - ​定义：小规模（通常<50 bp）的插入或删除。
    - ​影响：可能导致移码突变（frame-shift），破坏阅读框，改变下游氨基酸序列。
    - ​速率：人类中发生率约为点突变的1/10，约每代每碱基 $1 \times 10^{-9}$。
6. ​结构变异（Structural Variation, SV）​
    - ​类型：
        - ​拷贝数变异（CNV）​：重复或缺失大片段的DNA（>1 kbp），例如果蝇中唾液淀粉酶基因的串联重复。
        - ​染色体易位、倒位：由不等交换或转座子活动引起。
    - ​速率：低于点突变，人类中约每代每个体0.1次大片段CNV。
7. ​染色体变异
    - ​多倍化​（如植物中的全基因组重复）和非整倍性​（如人类唐氏综合征，21号染色体三体）。
    - ​速率：多倍化在植物中常见，但在动物中罕见；非整倍性在人类中发生率为约1/1000新生儿。

遗传多态性的应用：
- 推断群体历史
- 检测自然选择

编码区点突变的类型：在蛋白质编码区，点突变根据对氨基酸序列的影响分为以下类型：
1. ​同义突变（Synonymous Mutation）​
    - 碱基替换后编码的氨基酸不变（如密码子第三位的突变）。
    - ​例：CGA（Arg）→ CGG（Arg）。
2. ​非同义突变（Non-synonymous Mutation）​
    - 碱基替换导致氨基酸改变，包括：
        - ​错义突变（Missense）​：氨基酸类型改变（如CGA→CCA，Arg→Pro）。
        - ​无义突变（Nonsense）​：产生提前终止密码子（如CGA→TGA，Arg→终止）。
3. ​调控区突变
    - 发生在启动子、增强子等非编码区，影响基因表达水平。
    - ​例：人类MYH16基因调控区突变导致咀嚼肌缩小，可能与脑容量扩大相关。

其他重要突变机制
- ​转座子活动：如LINE-1（L1）介导的逆转座导致基因重复或调控区插入（例如果蝇Ssk-FB4嵌合基因）。
- ​重组相关变异：病毒通过重组获得新功能（如SARS-CoV-2的刺突蛋白RBM区域通过重组获得感染人类能力）。

群体遗传与基因组数据分析

### 群体进化历史推断

利用遗传多态推断群体历史
- 构建群体进化关系：Mit-DNA、Y-Chromosome (NRY)
- 推断群体大小动态
	- 单群体历史
		- 等位基因频谱 (AFS)
		- PSMC
	- 多群体历史
		- 联合等位基因频谱 (JAFS)
		- MSMC
		- G-PhoCS

从谱系到遗传多态数据：多篇论文，Heng Li & Richard Durbin
- infinite sites model
- infinite alleles model
- finite allele model

## 自然选择检测与推断

自然选择 (natural selection)：达尔文
- 加拉帕戈斯群岛 (the Galapagos islands)
- 达尔文雀：自然选择在起作用的例证
- 蛾子的工业黑化
- 理论：过度繁殖、生存斗争、遗传变异、适者生存
- 类型：
	- 正选择
	- 负选择
	- 平衡选择
	- 背景选择
- 自然选择在基因组留下印记：等位基因频率的变化（遗传多态性的变化）
- hitchhiking effect
- 正选择检测：
	- Within species
		- Allele frequency spectrum 等位基因频谱
			- CLR test
				- **Nielsen's CLR test**
				- **Chen's CLR test**
					- selective sweep
			- **Tajima’a D test**
			- Fu and Li’s test
			- **Fay and Wu’s H test**
		- Haplotype structure 单倍型结构
			- **EHH test**
			- **iHS test**
			- **XP-EHH test**
			- **HMM-Sweep**
			- HaploSweep
		- Population differentiation 群体分化
			- **Fst**
			- PBS
			- T-statistic
			- **XP-CLR test**：基于群体间分化检测自然选择的方法
				- 多个位点群体间频率差异，检测自然选择功效
				- 选择为点的惊喜定位
	- Between species
		- HKA test (Hudson, Kreitman, Aguad'e)
			- 假设：位点间独立、位点间无重组、两物种T代前从一个单一的祖先群体分化而来
			- 参数：突变速率、分化时间（$T$ 代之前分化）、$N, Nf, (1+f)N$
		- **McDonald Kreitman (MK) test**
			- data (1991)
			- 卡方检验
		- HDMKPRF
			- model
				- 参数：有效群体大小，selection intensity，突变速率，分化时间 (divergence time)
			- framework
				- 泊松分布
				- Poisson random field framework
				- MCMC steps for parameter optimization
					- Forward simulation with under positive selection and negative selection
					- Evaluating the performance
					- False positive rate
					- Convergence diagnosis for MCMC
			- Comparing results with MK test
				- Gene set enrichment analysis
		- Kreitman-McDonald test
		- CEGA：模型构建
			- 模型参数：全局参数、位点特异的参数
			- 最大似然法参数求解
			- 仿真实验：正向选择、平衡选择
- 人与黑猩猩比较分析
	- 人类分支
		- 正选择基因富集分析：通路、疾病、GO
		- 非编码区正选择基因富集分析：通路、疾病、GO
		- 平衡选择基因富集分析：通路、疾病、GO
- 不同方法的时间尺度
- 正选择性状例子：
	- 肤色进化：SLC24A5, OCA2
	- 高原适应：EPAS1
	- 乳糖耐受
- The genomics of selection in dogs and the parallel evolution between dogs and humans
- Hard sweep vs Soft sweep
- 背景选择 (background selection)

# 进化遗传学

## 遗传变异

遗传变异的起源：基因型空间的塑造机制
- 基础知识：中心法则、基因结构
	- 遗传变异 (genetic variation)
	- 突变 (mutation)
		- 多数有害
		- 固定到物种的有利突变为野生型 (wild-type)，即正常基因
		- 频发突变 (recurrent mutation)：一个重复发生的特定突变
- 基本类型：
	- 小变异 (small-scale sequence variation, < 1Kbp)
		- 核苷酸替代 (substitution)
		- 单核苷酸多态 (SNP) / 点突变 (point mutation)：数量大、鉴定容易，研究很多
			- 转换 (Transition)：在 purines/pyrimidines 内部
			- 颠换 (Transversion)：在 purines/pyrimidines 之间
			- 成簇SNP (cSNP)：修复错误导致，一次突变事件的结果
			- 同义/沉默 (synonymous/silent)：编码区 24% 为同义突变
				- 密码子中第三个位点 (摇摆位置/简并位点, wobble position)：70% 概率沉默
				- 四倍简并位点
			- 非同义/错义 (nonsynonymous/missense)
			- 无义 (nonsense)
		- 插入/删除 (indel, < 50bp)
			- 常见于微卫星 (microsatellite) 区域
			- 移码 (frame-disrupting) indels：最为有害，因而在群体内频率最低
				- 补偿性突变 (compensatory mutation)
				- 回复突变 (back mutation)
	- 结构变异 (large-scale structural variation, > 1Kbp)：
		- 重组导致的结构变异
			- 不等交换 (unequal crossing over)
				- 在一个重组产物上形成串联重复 (tandem duplicaiton)
				- 另一个重组产物上产生缺失
			- 非等位基因同源重组，导致三类结构变异
				- 删除/复制
				- 倒位
			- 重组导致新单倍型：增加突变的输入
				- 单倍型 (haplotype)：不同等位基因或不同突变的组合
					- 异位互作 (epistatic interaction)
		- 拷贝数变异 (copy number variation)
			- 拷贝丢失 (Copy number loss)
			- 拷贝获得 (Copy number gain)
		- 重排 (Rearrangement)
			- 易位 (Translocation)
				- 非同源染色题联会
			- 倒置/倒位 (Inversion)
			- 单亲二体 (Segmental acquired uniparental disomy)：癌症生物学中称为 loss-of-heterozygosity (LOH)
		- 转座子
			- LTR：导致RNA水平的重复
			- DNA转座子：导致DNA水平的基因重复
		- 重组或复制出错导致的简单串联重复
			- 不同基因组存在突变偏好
			- 蛋白复合体基因：较少发生完整重复，因为共同的选择压力导致的剂量敏感
		- 复杂结构变异 (complex SV)：复制错误导致，多个位点
			- 一次突变事件同时带来了重复和删除
	- numerical variation (whole chromosomes or genomes)
		- 多倍化 (polyploidy)
			- 导致全基因组扩增 (whole genome duplication, WGD)：植物中常见
				- 2R假说：脊椎动物起源
				- WGD导致适应性上升：面对选择压力改变
			- 核型 (karyotype)：染色体数目、大小分布
				- 快速演化
				- 重复序列重组导致染色体融合
		- 非整倍性 (aneuploidy)：唐氏综合征
- 突变速率
- 非典型突变：体细胞变异

遗传变异的检测
- 二代测序（以Illumina为代表）​
	- 优点：
		1. ​高精度：单碱基错误率低（<0.1%），适合检测单核苷酸多态性（SNP）和小插入/缺失（Indel）。
		2. ​高通量：单次运行可产生数十亿条短读长（如2×150 bp），成本低（每Gb约$0.01），适合大规模测序项目。
		3. ​成熟技术：标准化分析流程完善，广泛应用于全基因组测序（WGS）、外显子组测序（WES）、转录组测序（RNA-seq）和表观遗传学（如ChIP-seq）。
	- 缺点：
		1. ​短读长（50-300 bp）​：难以跨越重复序列或复杂结构区域（如转座子、基因家族），导致基因组组装不完整（碎片化）。
		2. ​PCR扩增偏差：扩增过程中可能引入GC含量偏好性误差，导致覆盖不均（如高GC或高AT区域漏检）。
		3. ​无法解析复杂变异：对长串联重复、倒位、易位等结构变异（SV）检测能力有限。
	- 典型应用：
		- 临床诊断（癌症基因panel、遗传病筛查）、群体遗传学（GWAS）、微生物多样性分析。
- 三代测序（以PacBio SMRT和Oxford Nanopore为例）​
	- 优点：
		1. ​超长读长（10 kb–100+ kb）​：直接跨越重复序列、复杂结构区域和基因组缺口，显著提升组装连续性（如人类T2T基因组N50达Mb级）。
		2. ​无需PCR扩增：直接测序保留天然DNA甲基化信息（如5mC、6mA），支持表观遗传学分析。
		3. ​解析复杂变异：精准检测结构变异（SV）、基因融合、转座子活性及全长转录本异构体（如选择性剪接）。
		4. ​实时测序（Nanopore）​：便携式设备（如MinION）支持野外或临床现场快速测序（如病原体即时检测）。
	- 缺点：
		1. ​高原始错误率：
		    - PacBio：原始错误率~10%，但通过HiFi模式（环形一致性测序）可降至<0.1%。
		    - Nanopore：原始错误率5-15%，需依赖高覆盖或纠错算法（如Medaka）提升准确性。
		2. ​成本较高：每Gb成本约$10-100（HiFi模式更贵），适合靶向测序或小型基因组。
		3. ​数据分析复杂：需专用工具（如Canu、Flye组装）和高性能计算资源。
	- 典型应用：
		- 新物种基因组组装（如动植物、微生物）、癌症基因组结构变异解析、全长转录本测序（Iso-Seq）、宏基因组复杂群落分析。

技术对比与互补策略

| ​**指标**     | ​**二代测序**         | ​**三代测序**                      |
| ----------- | ----------------- | ------------------------------ |
| ​**读长**     | 短（50-300 bp）      | 长（10 kb–100+ kb）               |
| ​**单碱基准确性** | >99.9%            | PacBio HiFi >99.9%；Nanopore需纠错 |
| ​**通量/成本**  | 高通量、低成本（$0.01/Gb） | 低通量、高成本（$10–100/Gb）            |
| ​**优势场景**   | SNP/Indel检测、群体测序  | 复杂基因组组装、结构变异解析                 |

互补策略：
1. ​混合组装（Hybrid Assembly）​：结合二代短读长（纠错）和三代长读长（骨架搭建），提升组装质量（如人类T2T基因组）。
2. ​靶向富集测序：使用探针或CRISPR捕获目标区域，结合三代测序解析复杂变异（如癌症基因的融合事件）。

最新进展
1. ​PacBio HiFi：通过环形一致性测序（CCS）实现高精度长读长（10-25 kb，错误率<0.1%），接近二代测序水平。
2. ​Nanopore自适应采样：实时选择目标序列测序（如病原体基因组），节省数据量并降低成本。
3. ​单细胞+三代测序：解析单细胞水平的全长转录本和表观遗传异质性（如神经元多样性研究）。

总结：
- ​二代测序：适合高精度、低成本的大规模变异检测和成熟应用（如临床诊断）。
- ​三代测序：在解析基因组复杂性（重复序列、结构变异）和全长转录本分析中不可替代。
- ​未来趋势：两者结合（混合测序）将成为复杂基因组研究和精准医学的主流方案。

## 突变速率

速率估计方法
- 基于表型：但大部分表型变异都是多基因的 (polygenic)
- 基于序列比较
	- 新生儿与父母比较 (tiro study)
		- 家系测序 (trio-sequencing)
	- 突变速率=进化速率，中性理论
	- 突变积累品系 (mutation accumulation, MA)：通过最小化自然选择的力量，让心法突变自由积累
- 基于家系 (trio) 测序的突变速率估计逐渐增多

不同类型突变的速率估计
- 点突变速率和Indel：速率大抵在$10^{-9}-10^{-11}$之间，前者约是后者的10倍
- CNV速率：大抵在$10^{-7}-10^{-5}$之间
	- 也有工作估计CNV速率$10^{-6}-10^{-4}$之间
	- 单位点发生频率很高，且可影响更多碱基

新发突变适合度的分布 (fitness landscape)：大抵是有害或近中性
- 经过实验的物种：荧光假单胞菌、酵母、果蝇
- 影印接种法：突变（包含适应性突变）是随机发生的，而非环境诱导

突变
- 随机性：双重含义
	- 无法预测哪个拷贝会经历突变，即无法精准预测
	- 环境不会诱发适应性突变
		- 但不同突变对环境的适应性不同，有害突变的概率远高于有益突变
- 偏好性：随机性不意味着基因组中所有位置发生突变的机会均等
	- C$\rightarrow$T突变偏好
		- 点突变偏好：可为推断病毒未知的宿主提供参考信息
		- CpG点突变偏好
	- 微卫星序列的高indel突变率
	- 串联复制的高重复率
	- 复制滑移 (replication slippage)：改变微卫星重复个数的过程，突变率远高于每个碱基对的点突变率
	- 突变偏好反映自然选择？
		- 突变偏好与自然选择共同导致调控区的趋同进化
	- Indels附近的点突变速率上升
	- 差异较大的位置易积累更多突变 (Feedforward loop)
		- 父母亲本杂合区间易于积累新的点突变或者indel
	- 环境压力导致突变速率上升（特别是父系）
		- 快速积累的证据显示环境压力可提升相关基因的突变率
			- 转录诱导下的DNA修复 (Transcription coupled DNA-repair)
		- 人类点突变速率估计
			- 雄性驱动的演化 (Male driven evolution)：通过精子带入种群的新突变要多于通过卵子带入的突变
			- 成簇SNP随母亲年龄增加不断增多
		- 单细胞群体适应性进化多由新发突变驱动
		- 对于多细胞物种而言，个体数目有限，突变积累较慢，选择更多的作用于先前存在的突变
- 其他性质

非典型变异
- 体细胞突变 (Somatic mutation)：在癌症中普遍发生
	- 染色体碎裂 (Chromothripsis) 导致了癌症的出现
	- 非入侵性产检 (NIPT) 的兴起，检测唐氏综合症等疾病
	- 每个人都是嵌合体 (mosaic)，发育中同样存在突变与选择
	- 神经组细胞具有很高的点突变速率
		- 脑发育过程中的体细胞转座依然有待研究
	- 缺爱，导致转座子插入变多
	- 生殖系突变可以被体细胞突变所补偿
- 水平基因转移 (Horizontal gene transfer，HGT)：
	- 演化中的重大水平基因转移事件
	- 水平基因转移频繁发生，可以有功能后果
	- 拉马克主义 (Lamarckism) 的复兴？获得性性状 (Acquired trait, use or disuse)
- 表观变异：精子不仅仅是DNA的携带者，可介导表观遗传 (epigenetic inheritance)
	- 高脂饮食的小鼠其后代易于肥胖，由tsRNA介导

# 进化发育生物学

进化和发育：表型空间的塑造机制与演化规律

动物结构 (animal architecture)：现代的体态来自古代的设计 Modern Forms, Ancient Designs
- Modularity: repeated parts
	- 化石证据显示身体设计的模块化（宏观层面多个相似的器官）有着古远的历史
	- 串行同源物（同一个体内经过重复但略微不同的发育过程而产生的相似但又有差别的身体结构）
	- 现生生命也是类似的
- Symmetry and polarity 对称性和极性

## 发育遗传学初步

Monsters, Mutants, and Master Genes：主控基因和大突变的稀有性
- Natural variation of morphology
	- 同源异形：数目改变，类型改变
	- 达尔文式微小、渐进的进化为主；大的进化跃迁近乎不可能
	- 有希望的魔鬼：指代推动发育的基因所发生的突变，有可能带来大的表型改变，从而驱动新物种的起源
- Existence of master or toolkit genes (homeotic genes)
	- 同源异形基因（homeotic）存在的证据
	- Operon and switch (enhancers)
	- 顺式调控元件 (cis-regulatory elements, CRE)为基因附件DNA上的调控序列，包含增强子(enhancer)、抑制子(silencer)等
	- Hox genes shape the development of fruitfly
		- Hox genes unite animal development
		- 关键基因（master gene）如Hox在动物体系中指导了体态的发育
	- Hedgehog is important for the cuticle development 关键基因Hedgehog对表皮的发育很重要
		- Hedgehog as a demo case of biomedicine study
		- Hedgehog对于生物医学研究的意义
	- Tool kit gene classification
		- 工具箱基因（tool kit）：指定身体形成和形态建构的核心基因，包含Hox等转录调控因素、激素及色素合成等基因
		- The tool kit paradox and the origin of diversity
			- 人类、大猩猩整体上同源DNA的一致性为98.5%左右；Indel，SV方面的差别更大。

From E. coli to Elephants: All life forms are descended from a common ancestor
- 中心法则：古老而保守的设计

工具箱基因
- Making Babies: 25,000 Genes, Some Assembly Required
	- Fate is determined by the tool kit proteins 胚胎命运的指定
	- Fine regulation via combinatory logic 多个转录因子对顺式元件的组合可实现高分辨率的调控
	- Binding motif and combinatory power
		- 转录因子的结合序列通常比较短，可调控多达上千个下游基因。
		- 500个转录因子中任意两个的组合可能性数目惊人。
		- 而人类基因组编码超过1000个转录因子，组合调控的复杂度更高。
			- KRAB可能大多都调控转座子
		- Making distinct wings via differential regulation of a tool kit gene, Ubx
	- Developmental network
		- 包含转录因子和顺式调控元件的局部环路互相连接，进而组成有层级的网络
- The Dark Matter of the genome: Operating Instructions for the Tool Kit

调控演化驱动形态演化
- The Big Bang of Animal Evolution
	- Simple animal form before Cambrian Explosion 寒武纪之前的动物体态相对简单
	- Big bang of animal forms 寒武纪出现了各类体态
	- Regulatory evolution drives the big bang
		- Hox顺式调控元件的进化驱动了形态演化。
		- 寒武纪地层化石多样性的大量增加可以解读为遗传上的可能性（Hox基因的数目已经比较多）与生态机会碰撞推动的形态演化的结果。
		- The rapid diversification of animals in the early Cambrian is likely to have been the result of a complex interplay of biotic and abiotic processes
- Little Bangs: Wings and Other Revolutionary Inventions 顺式调控进化的重要性（模块化，修补、多功能、冗余）
	- Hox基因的数目多少决定体态的复杂性？
		- 新结构和新体态的进化需要新的基因？
		- 昆虫复杂体态的起源由Hox基因数目的增多来驱动
	- Ancient origination of Hox genes
		- Hox基因有着古远的起源(deep origin)，长期以来维持10个左右；
		- 各种无脊椎动物的复杂体态与Hox基因的数目增多无关
	- Shifting Hox expression in vertebrate evolution
		- Hox (Hoxc6) 基因表达模式的演化推动了颈椎的演化
	- Evolution of insect wing via genetic switches
		- 顺式调控元件的进化驱动了Hox在不同物种间的重新指定，即鳃状结构减少并特化为鳞翅目的前后翅。
- How the Butterfly Got Its Spots
	- 形态演化的大趋势之一为特化：漫长的演化长河中，重复的单元数目变少，功能分化。
	- Batesian mimicry：眼点对于蝴蝶具有重要的生态适应意义
		- Distal-less gene switches：Distal-less是Hox之外的核心基因之一，其顺式元件的演化驱动了眼点的起源。
		- In the eye of one taxpayer：科学发展过程的不确定性

肤色与脑演化
- Paint It Black
	- Fitness of zebra coloration 斑马的条纹影响适合度
	- Protein-level evolution of MC1R determines melanism in mammals and birds 黑皮质素受体的蛋白演化影响了哺乳动物和鸟类的肤色
		- Pleiotropy of MC1R MC1R影响多个性状（整合/integration）
- A beautiful Mind: The Making of Homo sapiens
	- Brain evolution：
		- 人脑与其他高等动物的脑无本质区别
		- Does loss of MYH16 drive brain expansion?
			- 另有文献报导MYH16的丢失发生在4-5百万年前，与化石显示的脑扩张发生的时间不符
			- MYH16不是单纯的基因丢失，实际上它断裂（fission）为人特异的两个小蛋白，并受正选择压力的作用
		- Does FOXP2 drive language origination?
			- 文献报导两个氨基酸的改变可影响下游几十个目的基因！
			- Foxp2并没有近期正向选择信号，但它对我们人类生物学依然是重要的

生命演化的恢宏与壮美 Endless Forms Most Beautiful
- Principles of evolutionary renovation 演化中创新的基本原则：
	- 修补 (tinkering)：修补概念的最早提出
		- 自然选择绝非工程师，没有蓝图，并不完美；
		- preadaptation/exaptation，teleological ?
	- 多功能 (multifunctionality)
	- 冗余 (redundancy)
	- 模块化 (modularity)
- Evo Devo: a new revolution
	- Evo Devo应作为一个更现代的综合进化论的支撑点
		- On Descent with Modification (达尔文物种起源的论断之一)
		- The Tools for Making the Kingdom Are Ancient 工具箱基因的古老起源
		- 调控演化推动形态的演化
		- 老基因的修补是革新的基础
		- 种内进化和种间进化有共同基础
	- Evo Devo and the teaching of Evolution 教授进化发育生物学的重要性
	- Evo Devo and animal conservation，Evo Devo和保护生物学
	- Voice from another Evo Devo big bull：Dr. Stern对进化与发育的互动做了更具体的描述

调控演化：
- Change of cis-regulatory element of the middle layer genes drive morphological evolution
	- 网络中间层基因的调控演化更为重要，网络如何定义，中间层如何定义？
- Cis-regulatory mutation wins in long-term morphological evolution
	- 基因丢失突变更多影响短期进化中的表型演化，调控演化倾向于影响长期进化中的形态变化。

## Evo Devo 1.5

进化的两个层面：on genes and form

物种之间胚胎
- Species are more similar as embryos than as adults 物种之间胚胎发育的相似性
	- Karl Ernst von Baer
- Does ontogeny recapitulate phylogeny? 个体发生重现系统发生？
	- 祖先的成体状态很少在后代个体发育中重现
	- 后代不同发育阶段的发育速率经常与祖先不符（异时性）
	- 后代需要与环境相符的适应性演化
	- 末端添加 vs. 幼态持续

进化中的发育规则 Developmental principles of evolutionary change
- 个体特化 (individualization)
	- 原始的鲸类和现代海豚
	- Individualization and loss of individualization occurs via evolving genotype-phenotype map
		- 分割 (parcellation)
		- 整合 (integration)
		- 基因型-表型映射的演化
- 解关联 (dissociation)
- 异时 (heterochrony): an evolutionary change in the timing or rate of developmental events.
	- 祖先状态
	- 过量生长
	- 初期发育
	- 加速生长：不同器官
	- 幼态持续（卖萌）：蹼足
- 异地 (heterotopy): changes in the cells or tissues in which gene action or other developmental events occur.
	- 在两海胆近缘种中，表达Meso1的细胞不同
	- 突变热点与自然选择共同导致调控区的趋同进化
	- Distal-less gene switches
		- Hox之外的核心基因之一的Distal-less的顺式元件的演化驱动了眼点的起源
- 互作 (developmental interactions)
- 阈值 (thresholds): complex dynamic systems (nonlinear properties). crossing a threshold, lead to discontinuous differences in other components.
	- 脊椎动物体节分节“时钟”
- 模式 (pattern formation): the process by which the spatial pattern of cellular differentiation is specified.
- 弹性 (plasticity) Developmental plasticity and integration
	- 系统整合 (integration)：演化优势
		- Developmental integration 发育整合的意义：
			- origination of a retrogene largely accounts for chondrodysplasia of dogs
			- : origination of a retrogene largely accounts for height of dogs
			- evolution of visual system 眼睛和视觉中枢的发育偶联
	- 发育弹性
	- Canalization 渠化：a measure of the ability of a population to produce the same phenotype regardless of variability of its environment or genotype
		- C. H. Waddington (1957)
		- Canalization buffers internal and external variance 渠化减少了表型变异，使得选择失去了作用对象
		- 生物体系可缓冲突变 (buffer mutation)，环境压力改变时，缓冲体系丧失，突变得以释放
- Hox
	- Hox gene number evolves，Hox基因的扩增
	- Significance of Hox for evolutionary biology
		- hardly overstate the importance
		- vertebrates and invertebrates
		- conserved, as opposed to evolving
	- Ancient origination of Hox genes
		- Hox基因有着古远的起源 (deep origin)，长期以来维持10个左右；各种无脊椎动物的复杂体态与Hox基因的数目增多无关

同源性 (homology)
- homology vs. homoplasy
	- 同源：来自共同祖先
	- 一致性
	- 类似，非同源相似
	- 性状两次起源
- 非同源相似变异：趋同进化、平行进化、进化逆转 (evolutionary reversal)
- 发育同源：同源根据不同的上下文有不同的定义
- 重复结构：模块化
- Does biological homology exist?
	- 演化上同源的器官或许有不同的发育或遗传的基础
	- 非同源器官可共享同源的遗传基础
	- 基因重复干扰了基因功能的映射关系
- The concept of biological homology
	- 生物学同源性状可定义为某特化的结构单元在个体进化中的建立和保守性
	- 遗传层面的系统发生关系和形态发生未必对应；性状可以保守，而其遗传、发育的程序已经变化
	- 征召 (recruited or co-opted) exaptation, tinkering
- Phenotypic stasis vs. genetic changes
	- 性状的保守性并不代表遗传层面的保守性：
		- even-skipped (eve) 基因是一个“成对”规则的基因，在胚胎中表达形成七个条带，每隔一个体节形成一个条带。
		- 所有5个物种的Even striped-2序列在黑腹果蝇中都驱动2，3，7条带的表达，但其上游的调控序列（增强子）在物种间差别极大。
- Seemingly evolutionary stasis

发育如何约束进化？
- 未曾演化出现的可能表型，为何它们从未出现？为何有些性状难以演化出来？
	- 遗传层面缺乏相应的变异
	- 性状可能有害，净化选择压力将其淘汰
	- 缺乏支撑该性状的发育基础
	- 性状间的相互关联，导致某一性状难以自由演化
- Genetic constraint & phylogenetic constraint
	- 进化生物学和发育生物学曾长期分离
	- 物理、功能乃至发育约束会导致一系列的后果
		- 缺乏性状
		- 某些演化方向更可能发生
		- 共同的生态压力或发育约束皆可导致平行演化
			- 趋同进化 vs. 平行进化：有时，趋同进化和平行进化并不细分
		- 性状在种系历史的早期演化快，后期发育约束越来越大
		- 演化速度下降
		- 发育早期的改变会影响后期的发育程序，因而早期的演化速度下降
	- 除正向自然选择与突变偏好外，发育约束应该也存在，使Pitx1调控区的改变成为为数不多的解决方案之一
	- Absence of features
		- 性状的整合（integration）导致缺乏相对独立的发育程序，因而蝴蝶不能发育出具备不同颜色的眼点
	- Rule of Seven
		- Hox基因的组合调控指导了哺乳动物颈椎的发育
		- Hox基因的组合调控导致了相互约束，使脖子形状的演化依赖于某个特定椎节的变化，而不是像其它脊椎动物那样改变椎节的数目
		- Shifting Hox expression in vertebrate evolution
			- Hox (Hoxc6) 基因表达模式的演化推动了颈椎的演化
	- 高原雪雀DTL基因非同义突变富集于WD40结构域之外的区域
		- 与同义突变（中性背景）和低地生活的树麻雀相比，祖先与三个子代雪雀物种（adamsi, rufico, taczan）维持了同样的序列演化偏好，可能由于发育约束导致

## 基因的获取和丧失

when gene gain and gene loss occurs in the development
- Gene content evolution are underappreciated partiallydue to the propaganda of Evo Devo. 
- Integrative omicsdemonstrated the prevalence of gene gain/loss andtheir roles in phenotypic evolution, especially indevelopmental evolution.
- 基因的起源、丢失也可以驱动发育的进化。
- Terminology
	- Synonyms: young gene, gene origination, gene gain or gene birth
	- Synonyms: gene death, gene loss
- 物种具有大量种系特异基因
- 物种间的比较基因组可用于推断基因的起源年龄进而鉴定种系特异的基因
	- 比较基因组和系统发育组揭示无颌类与有颌类脊椎动物只共享一轮全基因组重复 (1R) ，后继分别发生谱系特异的WGD (2R与CR)
- Gene gain is prevalent
- 直系同源（Ortholog），旁系同源（paralog）
- Tinkering vs de novo
	- 修补概念
	- 相信修补论（tinkering）的Jacob认为蛋白的从头起源是不可能的
- evolutionary renovation
	- 演化中创新的基本原则：修补、多功能、冗余、模块化
- 新蛋白编码基因可从头起源（de novo origination）
	- 剪切结构（Splicing structure）
- How evolution builds genes from scratch
	- A trait may be difficult to be built from scratch. So it emerges by tinkering (from A to B). But for genes especially for relatively small genes encoding fewer than 200 or even fewer than 100 amino acids, they could emerge de novo
	- XIST emerges via transformation
		- 非编码RNA可来自丢失蛋白编码能力的假基因。如全基因组共线性比对显示X染色体失活调控基因XIST来自假基因化的Lnx3
	- Pseudogene as miRNA sponge?
		- 假基因在疾病状态（如癌症）中，更有可能发挥调控角色；
		- 它们在正常的发育或生理过程中，较少执行功能
	- Numerous loss-of-function (LoF) mutation could destroy one gene
		- Less is more? （少即是多假说）
		- 典型的人类个体基因组含有100个功能丢失突变（如破坏读码框的indel），绝大多数并没有显示正选择信号
		- “少即是多”模型在植物体系更为可能？
			- 与人相比，植物中的功能丢失突变（如破坏读码框的indel）更多地显示正选择信号，可能有生态适应的意义

Mutational mechanism leading to gene gain and loss
- Rate of gene gain
- Various mechanism
	- RNA水平的基因重复
	- DNA水平的基因重复
	- 非等位基因同源重组（non-allelic homologous recombination）可导致三类结构变异（Structural variation）
	- LTR类型的逆转座子可导致RNA水平的重复，DNA转座子可以导致DNA水平的基因重复
	- 外显子重排(exon shuffling)/基因融合
		- 外显子重排概念提出的逻辑基础：
			- 外显子可对应于独立功能域（domain）；
			- 内含子区重复序列辅助下的重组可创造外显子的新组合
		- 内部基因重复(internal duplication)导致的外显子洗牌与可变剪切
			- 内部基因重复皆可导致可变剪切的出现，从而维持重复前的祖先转录本。
			- Gilbert同时提出了外显子洗牌和可变剪切的概念；这两个概念实际上是紧密相关的。
			- 类似的，基因重复与外显子洗牌传统上作为两个各自独立的机制；现在看起来，这两个机制也是紧密相关的。
	- 水平基因转移频繁发生，可以有功能后果：唯一能合成胡萝卜素的动物
	- Birth of monkey-king via gene fission 基因裂变通过基因重复和差别衰减实现
- Gene loss
	- Does loss of MYH16 drive brain expansion (continued)?
		- MYH16不是单纯的基因丢失，实际上它断裂（fission）为人特异的两个小蛋白，并受正选择压力的作用

Rapid birth followed by rapid death
- New genes may die out in some lineages during a prolonged pre-preservation stage
	- 果蝇中雄性年轻偏向基因富集于X染色体，后期逐渐丢失
	- 哺乳动物体系结果类似：
		- 多种模型如Faster-X假说、X染色体雌性化假说解释了X染色体编码的新雄性偏向基因的快速起源与快速丢失
- 突变机制约束或推动重复基因的功能演化
- All previous slides refer to small-scale mutations rather than whole genome/chromosome copy number change, change, which has special features (e.g. massive gene loss after duplication)

Developmental evolution driven by gene gain and death
- Method and application related with gene gain and loss
	- OR（嗅觉受体）在灵长类的丢失：生物无用结构退化
	- Inference of gene ages based on syntenic genomic alignment
	- Detection of orthologs
		- Ensembl pre-computed orthologous gene annotation
		- UCSC提供了模式动物体系的全基因组共线性比对，从这些比对中，可提出各物种的编码区及非编码区的同源序列
	- 用phylostratigraphy（基因的演化年龄分布）理解宏进化
		- 不同功能的基因有不同的年龄分布，例如发育中的转录因子在寒武纪之前即已经起源。
	- Ancient origination of Hox genes
		- Hox基因有着古远的起源(deep origin)，长期以来维持10个左右；
		- 各种无脊椎动物的复杂体态与Hox基因的数目增多无关
	- 种系特征性发育阶段（phylotypic stage）表达的基因起源年龄最为古老
		- phylotypic stage：隶属同一门的物种，胚胎发育中相互之间最像的阶段
	- 物理、功能乃至发育约束会导致一系列的后果
		- 发育早期的改变会影响后期的发育程序，因而早期的演化速度下降：应主要是phylotypic stage
	- Species are more similar as embryos than as adults
		- 物种之间胚胎发育的相似性：应主要是phylotypic stage
	- 胚胎发育中期种系特征性发育阶段的存在由高度整合的多效性基因网络导致
- New gene in fly development
	- Genome-wide age dating in D.melanogaster
	- New gene could be essential for Drosophila
		- The essentiality of new genes may be caused by the co-evolution of the whole molecular network
			- 新基因的出现伴随着新的调控原件（绝缘子）的起源
			- 新基因此前并不存在，自然也谈不上对物种的重要性。但当它起源之后，逐渐整合进分子网络，引起整个系统的共进化 (coevolution)
			- 因而当它们被敲除时，有可能引发系统性的崩溃，导致果蝇死亡
- New gene in human brain development. Could new gene be also manifested in human development?
	- Genome-wide age dating in human and mouse
	- Human brain demonstrates an excess of new gene expression relative to mouse
		- 各器官转录组中灵长类或啮齿类特异基因的比例分布
	- Primate-specific genes are upregulated in mid-fetal brain
		- 孕期12周到22周的新脑皮层中更多表达灵长类或人类特异的年轻基因
		- 考虑到这一时期表达的基因出错易导致自闭症，这些基因对脑发育演化的重要性可能是比较大的
	- 灵长类特异重复基因DDX11在胚胎期脑发育中上调
	- 灵长类特异基因（primate-specific genes PSGs，含人类特异基因human-specific genes HSGs）有较大的功能后果
	- 10个实验验证的驱动脑演化的人特异突变中新基因占了7个
		- GenTree serves as a community resource of new gene origination
	- 使我们强大的基因也有可能增加我们得病（特别是癌症）的几率
		- 年轻基因大多来自基因重复，其基因组位点不稳定，在癌症中很容易扩增
- Summary: new gene quickly invades into the developmental pathway of fly and mammals
- How about other species? 新基因的起源是表型演化的推动力之一，不仅限于人和果蝇，对于其他物种体系（开花植物）也是同样
	- Developmental integrity: origination of a retrogene largely accounts for the leg length variance in dog
	- Duplicate genes contributed to development of evolution of early vertebrates
		- Hox基因的扩增
		- 功能基因组揭示全基因组重复所产生的新基因导致发育程序的改变
			- 功能富集分析
- How about other genes? 与编码基因相比，非编码基因（miRNA，lncRNA等）的起源速率更快，物种或种系特异的年轻基因的比例更高
	- Duplicated pseudogenic HBBP1 plays human-specific essential role in red blood cell development.
		- 该重复基因在小鼠中已丢失，在黑猩猩中不表达，但在人类的红细胞发育过程中高表达，并发挥不可缺少的功能
	- Comparative omics revealed the generality of gene gain in evolution and the functional significance of new genes for fly development or human brain development. Thus, although there are deeply conserved tool kit genes, some of them may be quite young. Does it mean Evo-Devo is wrong?
		- New gene origination can also minimize the pleiotropy
			- Carrol之所以推崇顺式调控元件的演化，是因为这些元件模块化的设计使其本身的变化不影响其他调控元件的功能，最小化负向多效性（negative pleiotropy）；
			- 但基因重复或新基因的起源同样不影响其他拷贝或其它基因的功能。
		- Protein evolution vs. regulatory evolution
			- 蛋白层面的进化与调控的进化在表型进化中的贡献均等
		- The tool kit paradox and the origin of diversity
			- 人类、大猩猩整体上同源DNA的一致性为98.5%左右；Indel，SV方面的差别更大

遗传-发育-进化的统一
- 负向多效性的多少是突变是否能够固定的核心

Looking forward：生物学需要多个层面的研究

# 分子进化

进化生物学的时间尺度
- 宏进化 (Macro-evolution)
	- Focus: The differences between species Phylogenetics
	- Fields:
		- Systematics
		- Molecular Evolution
		- Comparative Genomics
- 微进化 (Micro-evolution)
	- Focus: The differences between individuals within a speciies
	- Fields: Population Genetics

## 数学基础

分子进化
- 概念：分子进化是指DNA、RNA和蛋白质等细胞分子在世代更替中序列组成发生改变的过程
	- 该领域运用进化生物学与群体遗传学原理阐释这些变化的规律
	- 分子进化是进化生物学的一个分支，专注于在DNA序列层面上研究进化变化
- 核心研究议题包括：
	- 单核苷酸突变的速率及其影响
	- 中性进化与自然选择的作用
	- 新基因的起源
	- 复杂性状的遗传本质
	- 物种形成的遗传基础
	- 发育机制的进化
	- 进化力量如何驱动基因组与表型变化
- 研究内容包括：
	- 序列变化的速率
	- 适应性突变与中性突变的相对重要性
	- 基因组结构的变化

生物信息学：早期历史的很多研究都是围绕着序列比对：
1. Margaret Dayhoff 于1978年定义了PAM (Point Accepted Mutation), 是一个20个氨基酸相互之间转变的替换矩阵（这里不赘述），这些研究推动后续的生物学信息学的快速发展。
2. Needleman-Wunsch (1970), Smith-Waterman 算法(1981), BLAST (1990, David Lipman etc), BLAT (2002, Jim Kent) 等等.
3. 随着基因组学，特别是人类基因组的测序，分子进化、基因组进化以及生物信息学做了深刻的融合。

随机过程 (Stochastic processes)
- 背景：随机变量是指随机事件的数量表现
	- Exponential distribution
		- 指数分布是刻画很多事件的很好的分布函数。例如银行柜台从上一个到下一个客户的等待时间，高速路上车子进入收费站的等待时间等
		- λ，又叫intensity parameter, 刻画了指数分布的特征， λ越大，等待时间就越短
		- Rate variation among sites
			- 不同位点的进化速率不是很一样，我们用一个随机分布来刻画不同位点之间的进化速率的差别，我们一般使用gamma distribution
	- Poisson process
		- Formal definition of Poisson process需要一些数学的setup.
		- 如果事件之间的等待时间都是指数分布(λ), 那记录事件数目随着时间累积的这个过程就是泊松过程
		- 给定一个时间段，发生事件的数目是一个λ*τ的泊松分布
- 定义：A stochastic orrandom process can be defined as a collection of random variables that is indexed by somemathematical set
	- 很多时候是$t$，时间或者自然数
	- 自然世界的很多现象都可以用随机过程来表征：例如每天的天气情况、某人的每天的血压等等
- Stochastic processes on trees
	- Gene genealogy and phylogeny

离散和连续时间的马尔可夫链
- 马尔可夫链（或马尔可夫过程）是一种随机模型，用于描述事件序列中每个事件发生的概率仅取决于前一个事件所处的状态
	- 根据时间是离散还是连续，状态空间是否有限 (countable)，马尔科夫链有很多不同的类型
	- 在序列演化里，我们状态空间一般都是有限空间(finite space)。
		- 例如，我们在碱基层次，都是A/T/C/G, 在密码子层面就是61/64密码子
	- 离散时间的马氏链
		- transition probability matrix
		- Chapman Kolmogorov Equation
	- A few key concepts from MC
		- Stationary distribution: The stationary distribution of a Markov chain describes the distribution of Xt after a sufficiently long time that the distribution of Xt does not change any longer.
			- Estimating evolutionary distance/time
		- Time reversibility

序列演化的系列模型
- Nucleotide substitution model
	- 需要一个进化模型刻画碱基替换的过程
	- 在分子进化里，我们使用马尔可夫链来刻画这一过程
	- 每个位点被认为是独立演化的
- 转移概率矩阵
- 转移速率矩阵
- JC69 model
- Kimura 2 parameter model (1980)
	- Estimating evolutionary distance/time
- Other nucleotide models
- Family of models

## 检测适应性进化的统计学方法

宏微观进化检测适应性进化的差别
- 在群体遗传学（微进化）里，我们主要研究种群内部的差别，体现自然选择的footprint (印记）主要是频率和遗传多样性等指标，这些内容在前面的课程里，已经有了比较好的学习。
- 在宏进化里，我们主要研究进化的结果，我们的主要的参数就是进化的速率（进化的数量)。 很多时候，我们需要找一个“putatively neutral segment”（近中性）的区段来比较我们的进化速率。我们从群体遗传学里知道，如果我们有适应性或者正选择的SNP, 这些位点会更快地固定下来，导致更高的进化速率

突变的效应(fitness effect)和进化速率
- The rate of evolution is a function of
	- Mutation rate
	- Selection intensity

dN/dS or Ka/Ks ratio
- Counting method
	- Challenges with counting methods
		- model dN/dS over a codon 密码子模型
			- Codon based likelihood model
			- Site models: Nested models
				- Logistics with the computation
				- Likelihood ratio test
			- Branch and branch-site models
			- human adaptation
- Counting # of nonsyn/syn differences
- Correct for multiple hits

## 如何构建系统进化树

建树方法：
- 距离法
	- UPGMA
- 简约法
	- 最大简约法 (maximum Parsimony)
- 似然法/贝叶斯法 Likelihood method
	- Likelihood of a tree
	- Testing of trees
	- Bootstrap resampling

### 3. 突变的速率、随机性及适合度分布

突变速率：突变速率因物种、突变类型和基因组区域而异，以下是主要类型的典型速率：
1. ​**点突变（SNP）​**：
    - ​**人类**：每碱基每代约 $1.2 \times 10^{-8}$，每个体每代约累积60个新点突变。
    - ​**果蝇**：速率较高，约 $3.5 \times 10^{-9}$ 每碱基每代。
    - ​**病毒（如SARS-CoV-2）​**：高频突变，例如刺突蛋白D614G突变在疫情期间快速扩散。
2. ​**插入/缺失（Indel）​**：
    - ​**人类**：速率约为点突变的1/10，每代每个体约6个新Indel，小片段（<50 bp）更常见。
    - ​**移码突变**：如人类CCR5Δ32突变（32 bp缺失导致移码），与HIV抗性相关，但可能伴随其他健康风险。
3. ​**结构变异（SV）​**：
    - ​**拷贝数变异（CNV）​**：例如果蝇唾液淀粉酶基因的串联重复，适应不同饮食环境。
    - ​**重组相关变异**：速率低，但影响显著，如SARS-CoV-2通过重组获得感染人类的能力（刺突蛋白RBM区域）。
4. ​**转座子活动**：
    - ​**LINE-1（L1）​**：人类基因组中最活跃的转座子，介导非自主元件（如Alu）扩增，导致基因重复或调控区插入。

突变的随机性：突变过程总体是随机的，但受以下因素影响而产生偏好性：
1. ​**序列依赖性**：
    - ​**转换（嘌呤↔嘌呤）​**：比颠换（嘌呤↔嘧啶）更常见，因DNA化学结构更易发生。
    - ​**微卫星区域**：短重复序列（如(AT)n）易发生滑动复制错误，导致Indel高频出现。
2. ​**基因组热点区域**：
    - ​**重组热点**：如人类HLA区域，因频繁重组导致突变积累。
    - ​**转座子活跃区域**：如端粒和着丝粒附近，转座子插入引发结构变异。
3. ​**修复机制偏差**：
    - ​**DNA修复效率差异**：转录活跃区（如基因启动子）修复更高效，突变率较低。
- **示例**：
	- ​**cSNP（成簇SNP）​**：由DNA修复错误导致，一次事件引发多个邻近位点突变，显示非完全随机性。
	- ​**逆转座介导的基因重复**：如果蝇Ssk-FB4嵌合基因，由DNA转座子FB4插入引发。

突变的适合度分布：突变对生物适合度的影响呈“L型分布”，即大部分突变有害，少数中性或有利：
1. ​**有害突变（占多数）​**：
    - ​**功能丧失（LoF）​**：如人类MYH16基因假基因化导致咀嚼肌缩小，可能伴随适应性代价。
    - ​**移码突变**：如CCR5Δ32虽提供HIV抗性，但可能增加其他感染风险。
2. ​**中性突变（次之）​**：
    - ​**同义突变**：不改变氨基酸序列，如四倍简并位点突变（密码子第三位）。
    - ​**非编码区突变**：如调控区轻微变异未显著影响表达水平。
3. ​**有利突变（极少）​**：
    - ​**适应性进化**：
        - ​**基因重复**：如人类唾液淀粉酶基因（AMY1）拷贝数增加，适应高淀粉饮食。
        - ​**结构变异**：如非洲爪蟾多倍化事件增强环境适应性。
    - ​**新基因起源**：
        - ​**从头起源（de novo）​**：如某些小基因（<100 aa）通过非编码序列演化获得新功能。
- **特殊案例**：
	- ​**​“少即是多”假说**：基因丢失可能带来适应性优势，如植物中功能丢失突变（如抗病基因缺失）在特定生态中有利。
	- ​**表型可塑性**：发育相关基因（如Hox）的突变可能通过阈值效应产生显著表型变化，例如果蝇Distal-less基因调控区演化驱动眼点形成。

自然选择与突变分布的相互作用
1. ​**纯化选择**：清除有害突变（如致死性LoF突变），但部分轻微有害突变在群体中保留（如平衡选择）。
2. ​**正向选择**：驱动有利突变扩散，例如果蝇JawH基因加速生长导致口器延长（适应捕食）。
3. ​**中性漂变**：中性突变在小群体中随机固定，如非编码区变异。
- **示例**：
	- ​**SARS-CoV-2突变D614G**：刺突蛋白突变增强传染性，在疫情期间被正向选择。
	- ​**异时性（Heterochrony）​**：发育速率改变（如蝾螈幼态持续）通过调控突变适应新环境。

​总结：
- ​**速率**：点突变 > Indel > 结构变异，病毒突变速率显著高于真核生物。
- ​**随机性**：总体随机但存在序列、修复和转座子介导的偏好性。
- ​**适合度分布**：大多数突变有害，少数中性或有利，自然选择是塑造突变分布的核心力量。
- ​**进化意义**：突变为进化提供原材料，但其适合度分布和随机性共同决定了自然选择的效率与方向。

---

### 4. 非典型突变：体细胞突变、水平基因转移与表观变异

体细胞突变（Somatic Mutation）​
- **定义**：发生在体细胞（非生殖细胞）中的突变，通常不遗传给后代，但可能影响个体发育或导致疾病。  
- **案例**：
	1. ​**癌症驱动突变**：
	    - ​**刺突蛋白突变（如SARS-CoV-2 D614G）​**：虽为病毒突变，但机制类似体细胞突变的积累（文档3）。
	    - ​**基底细胞癌**：因Sonic hedgehog（SHH）信号通路过度激活（如PTCH1受体突变），体现体细胞突变在肿瘤中的作用（文档4）。
	2. ​**发育异常**：
	    - ​**嵌合体（Mosaic）​**：体细胞突变导致同一生物体内不同细胞基因型差异，如果蝇复眼颜色嵌合体（文档未直接提及，但基因工具如FLP-FRT系统常用于研究）。
- **进化意义**：
	- 体细胞突变可能通过表型可塑性（如植物体细胞变异适应环境）间接影响进化，但一般不直接参与遗传。

水平基因转移（Horizontal Gene Transfer, HGT）​
- **定义**：跨物种的基因传递，常见于微生物，但在真核生物中也有发现。  
- **案例**：
	1. ​**植物-微生物基因转移**：
	    - ​**真菌类胡萝卜素合成基因**：蚜虫通过水平基因转移获得真菌的类胡萝卜素合成基因，使其体色变红（文档3）。
	2. ​**病毒介导的重组**：
	    - ​**SARS-CoV-2刺突蛋白RBM区域**：通过重组从穿山甲冠状病毒获得，增强对人类ACE2受体的结合能力（文档3）。
- **进化意义**：
	- 快速获得新功能（如抗逆性、代谢途径），绕过传统垂直遗传的缓慢过程。

表观遗传变异（Epigenetic Variation）​
- **定义**：DNA序列不变的情况下，通过甲基化、组蛋白修饰等机制调控基因表达的可遗传变化。  
- **相关机制**：
	1. ​**基因调控区突变**：
	    - ​**MYH16基因调控区缺失**：导致人类咀嚼肌缩小，可能与脑容量扩大相关（文档3），虽为DNA序列改变，但体现调控变异对表型的影响。
	2. ​**发育阈值效应**：
	    - ​**形态发生素（Morphogen）浓度阈值**：如Hedgehog信号通路中，微小浓度变化通过表观调控决定细胞分化（文档4）。
- **间接关联案例**：
	- ​**XIST基因起源**：由假基因Lnx3演化而来，通过表观沉默X染色体（文档3），体现非编码RNA的表观调控功能。
- **进化意义**：
	- 表观变异可快速响应环境压力（如温度、营养），通过表型可塑性促进适应性演化。

三类非典型突变的对比：

| ​**类型**     | ​**机制**      | ​**文档案例**           | ​**进化角色**      |
| ----------- | ------------ | ------------------- | -------------- |
| ​**体细胞突变**  | 体细胞DNA序列改变   | 癌症（SHH通路突变）、病毒适应性突变 | 个体适应，一般不遗传     |
| ​**水平基因转移** | 跨物种基因传递      | 蚜虫获得真菌色素基因、病毒重组     | 快速获得新功能，突破物种界限 |
| ​**表观变异**   | DNA甲基化/组蛋白修饰 | XIST基因调控、形态发生素阈值效应  | 环境响应，可遗传的表型可塑性 |

研究前沿与挑战：
1. ​**体细胞突变与衰老**：体细胞突变积累可能导致组织功能退化（如干细胞耗竭），但文档未深入讨论。
2. ​**真核生物HGT的频率**：除微生物外，植物和无脊椎动物中HGT的普遍性仍需验证（文档中案例较少）。
3. ​**表观遗传的跨代遗传**：环境诱导的表观变化能否稳定遗传仍存争议（如饥饿对后代代谢的影响）。

**总结**：非典型突变为进化提供了“快捷通道”，尤其在环境快速变化时，水平基因转移和表观变异可加速适应性演化，而体细胞突变则在个体生存中扮演关键角色。

---

### 5. Evo Devo学派的核心术语解析

Modularity（模块化）​
- **定义**：生物体在发育过程中形成功能或结构上相对独立的单元（模块），这些模块可独立演化，减少基因多效性（pleiotropy）的约束。  
- **体现**：
	- ​**体节（Somites）​**：脊椎动物胚胎中重复的模块化结构，每个体节独立发育为肌肉、骨骼等组织（文档1）。
	- ​**基因型-表型映射演化**：通过分割（parcellation）减少基因多效性，或整合（integration）形成新模块（图23.4，文档1）。  
	    - **进化意义**：模块化允许不同结构独立演化（如昆虫附肢与脊椎动物四肢），促进形态多样性。

Negative Pleiotropy（负多效性）​
- **定义**：单个基因影响多个表型特征（多效性），其中某些效应对适合度有害，限制基因的自由演化。  
- **关联**：
	- ​**基因型-表型映射的演化**：通过减少多效性（parcellation）实现模块化，避免负多效性对适应性的限制（文档1）。  
	    - **示例**：若某基因同时控制肢体发育和心脏功能，其突变可能导致适应性冲突，需通过模块化解耦。

Canalization（渠化）​
- **定义**：发育过程对遗传或环境扰动的缓冲能力，使得表型在变异中保持稳定。  
- **案例**：
	- ​**von Baer定律**：不同脊椎动物胚胎早期高度相似（如鳃弓结构），后期才分化，体现发育的渠化（文档1）。
	- ​**阈值效应**：形态发生素（如Hedgehog）浓度需超过阈值才会触发分化，缓冲微小变异的影响（图23.15，文档1）。  
	    - **进化意义**：渠化维持基本身体结构的稳定性，同时允许局部创新（如昆虫翅膀演化）。

Homology（同源性）​
- **定义**：不同物种的结构或基因因共同祖先而具有相同起源。  
- **案例**：
	- ​**Hox基因**：在果蝇和哺乳动物中调控体节极性，揭示动物形态的深层同源（文档1、4）。
	- ​**脊椎动物四肢**：从鱼类鳍到陆生动物四肢的同源演化（文档1）。

Homoplasy（同塑性）​
- **定义**：不同物种因趋同进化或平行进化产生的相似结构，但无共同起源。  
- **案例**：
	- ​**昆虫与鸟类翅膀**：独立演化出飞行结构（文档1）。
	- ​**鱼类的流线型体型**：鲨鱼（软骨鱼）与海豚（哺乳类）因适应游泳而趋同（文档未直接提及，但符合逻辑）。

Heterochrony（异时性）​
- **定义**：发育事件的时间或速率改变导致形态差异，是形态创新的重要机制。  
- **案例**：
	- ​**幼态持续（Paedomorphosis）​**：美西螈（Ambystoma）保留幼体特征（鳃和尾鳍）至成体（图23.2，文档1）。
	- ​**加速生长**：某些鱼类（如针鱼）因颌骨发育加速，演化出细长口器（图23.9，文档1）。  
	    - **进化意义**：微小的时间调整可产生显著表型变化（如人类脑容量的扩展可能与发育延迟相关）。

Tinkering（修补）​
- **定义**：进化通过修改现有结构（而非全新设计）实现创新，强调“旧零件的新组合”。  
- **案例**：
	- ​**基因重复与新功能**：唾液淀粉酶基因（AMY1）重复适应高淀粉饮食（文档3）。
	- ​**外显子洗牌（Exon Shuffling）​**：新基因通过已有外显子重组产生（如抗冻蛋白基因，文档3）。  
	    - **核心思想**：如François Jacob所述，进化是“修补匠”，利用现有材料创造新功能（文档3、4）。

总结：术语间的关联与进化意义

|​**术语**|​**核心机制**|​**进化作用**|
|---|---|---|
|Modularity|结构/功能独立化|减少多效性约束，促进局部创新|
|Canalization|发育稳定性缓冲|维持基本形态，允许阈值驱动的创新|
|Heterochrony|发育时序调整|快速产生形态差异（如幼态持续）|
|Tinkering|现有结构重组|低成本创新（如基因重复、外显子洗牌）|
|Homology vs. Homoplasy|同源起源 vs. 趋同演化|揭示深层演化历史 vs. 环境驱动的相似性|

**示例整合**：
- ​**Hox基因（Homology）​**：模块化调控体节发育，通过异时性（如时钟基因速率差异）导致蛇类体节增多（图21.20，文档1）。
- ​**Distal-less基因（Tinkering）​**：通过顺式调控区演化，在蝴蝶翅膀上产生眼点（文档1）。

这些术语共同构建了Evo Devo的理论框架，解释从基因到形态的演化逻辑。

---

### 6. 直系同源基因（Ortholog）与旁系同源基因（Paralog）的解析

定义与核心区别
1. ​**直系同源基因（Ortholog）​**
    - ​**定义**：因物种分化（Speciation）事件而产生的同源基因，存在于不同物种中，通常保留原始功能。
    - ​**进化机制**：通过垂直遗传（Vertical Descent）传递，功能保守性较高。
2. ​**旁系同源基因（Paralog）​**
    - ​**定义**：因基因重复（Gene Duplication）事件产生的同源基因，存在于同一物种或不同物种中，可能发生功能分化。
    - ​**进化机制**：通过基因重复后演化，可能亚功能化（Subfunctionalization）或新功能化（Neofunctionalization）。

案例与机制
1. ​**直系同源基因的案例**
    - ​**Hox基因家族**：
        - 果蝇与哺乳动物的Hox基因通过物种分化保留，调控体节极性（文档1、文档5）。
        - 例如，果蝇的_Antennapedia_基因与小鼠的_HoxB6_基因是直系同源，均参与体轴发育。
    - ​**刺突蛋白（Spike Protein）​**：
        - SARS-CoV-2与蝙蝠冠状病毒的刺突蛋白基因因物种分化形成直系同源，但D614G突变增强传染性（文档3）。
2. ​**旁系同源基因的案例**
    - ​**唾液淀粉酶基因（AMY1）​**：
        - 人类中通过串联重复（Tandem Duplication）产生多拷贝AMY1基因，适应高淀粉饮食（文档3）。
        - 不同拷贝（如AMY1A、AMY1B）为旁系同源，可能表达水平差异但功能相似。
    - ​**抗冻蛋白基因（Antifreeze Protein）​**：
        - 鱼类中通过外显子洗牌（Exon Shuffling）产生新旁系同源基因，适应极地低温（文档3）。

进化意义与功能分化：

|​**特征**|​**直系同源基因**|​**旁系同源基因**|
|---|---|---|
|​**起源事件**|物种分化|基因重复|
|​**功能保守性**|高（如Hox基因调控体节）|低（可能亚功能化或新功能化）|
|​**基因组位置**|跨物种同源区域|同一基因组内或跨物种重复区域|
|​**选择压力**|纯化选择维持功能|正选择驱动功能创新|

**示例对比**：
- ​**直系同源**：人类与小鼠的胰岛素基因（垂直遗传，功能保守）。
- ​**旁系同源**：人类血红蛋白α链与β链（基因重复后分化，分别结合氧气与二氧化碳）。

特殊情景与混淆点
1. ​**水平基因转移（HGT）​**：
    - 跨物种基因转移（如蚜虫获得真菌类胡萝卜素基因）属于异源同源（Xenolog），非直系或旁系同源（文档3）。
2. ​**基因家族扩张**：
    - 旁系同源基因的大规模重复（如嗅觉受体基因家族）是适应环境的关键机制（文档3）。
3. ​**假基因化（Pseudogenization）​**：
    - 旁系同源基因可能失去功能（如人类MYH16基因假基因化导致咀嚼肌退化，文档3）。

总结：
- ​**直系同源**是物种分化的“时间胶囊”，揭示深层演化关系（如Hox基因的跨物种保守性）。
- ​**旁系同源**是基因创新的“试验田”，通过重复与分化驱动功能多样性（如AMY1基因适应饮食变化）。
- 两者共同构成基因组演化的核心逻辑，直系同源维持生命蓝图，旁系同源拓展生态位适应。

---

### 7. 新基因起源的主要机制及案例解析

基因重复（Gene Duplication）​
- **机制**：通过DNA复制错误、不等交换或转座子活动产生基因的额外拷贝，为新功能演化提供原材料。  
- **案例**：
	- ​**唾液淀粉酶基因（AMY1）​**：人类通过串联重复产生多拷贝，适应高淀粉饮食（文档3）。
	- ​**Hox基因家族**：全基因组重复（WGD）导致基因数量扩张，调控脊椎动物体节分化（文档5）。  
	    **进化意义**：重复基因可通过新功能化（Neofunctionalization）或亚功能化（Subfunctionalization）适应新环境。

外显子洗牌（Exon Shuffling）​
- **机制**：通过重组或转座子介导的外显子重排，将不同基因的外显子组合成新基因。  
- **案例**：
	- ​**抗冻蛋白基因**：鱼类通过外显子洗牌产生新基因，适应极地低温环境（文档3）。
	- ​**人类凝血因子基因**：外显子重组形成复杂功能域（文档3）。  
	    **进化意义**：快速整合已有功能模块，产生多功能蛋白。

水平基因转移（Horizontal Gene Transfer, HGT）​
- **机制**：跨物种的基因传递，常见于微生物，真核生物中也有发现。  
- **案例**：
	- ​**蚜虫类胡萝卜素合成基因**：从真菌水平转移获得，使其体色变红（文档3）。
	- ​**SARS-CoV-2刺突蛋白重组**：通过重组穿山甲冠状病毒基因增强感染能力（文档3）。  
	    **进化意义**：绕过漫长垂直演化，直接获得适应性功能（如抗逆性、代谢新途径）。

从头起源（de novo Origination）​
- **机制**：非编码序列通过突变获得开放阅读框（ORF），演化出蛋白质编码功能。  
- **案例**：
	- ​**XIST基因**：由假基因Lnx3演化而来，调控X染色体沉默（文档3）。
	- ​**小基因（<100 aa）​**：从非编码RNA或随机序列演化，例如果蝇年轻基因（文档3）。  
	    **进化意义**：从零创造全新功能，推动形态或生理创新。

基因分裂（Gene Fission）​
- **机制**：单个基因分裂为多个独立基因，通常伴随功能分化。  
- **案例**：
	- ​**猴王基因（Monkey King）​**：祖先基因分裂为两个功能不同的旁系同源基因（文档3）。  
	    **进化意义**：精细化调控复杂通路（如发育信号网络）。

逆转座介导的嵌合基因（Retrotransposition）​
- **机制**：逆转座子通过RNA中间体复制并插入基因组，形成嵌合基因或新调控元件。  
- **案例**：
	- ​**Ssk-FB4嵌合基因**：果蝇中由DNA转座子FB4插入导致，可能参与应激响应（文档3）。
	- ​**人类Alu元件**：逆转座子介导的插入事件影响基因表达（文档3）。  
	    **进化意义**：快速产生新调控网络或嵌合功能蛋白。

进化意义总结：

|​**机制**|​**核心优势**|​**典型案例**|
|---|---|---|
|基因重复|保留原始功能，允许新功能演化|AMY1基因适应高淀粉饮食|
|外显子洗牌|快速整合功能模块|鱼类抗冻蛋白|
|水平基因转移|跨物种功能获取|蚜虫色素合成基因|
|从头起源|创造全新功能|XIST基因调控X染色体沉默|
|基因分裂|精细化功能分工|猴王基因功能分化|
|逆转座介导的嵌合|调控创新或嵌合功能|果蝇Ssk-FB4应激响应|

**关键结论**：新基因起源是演化创新的核心驱动力，通过“修补”（Tinkering）现有遗传材料或创造全新元件，生物得以快速适应环境挑战（如饮食变化、极端温度、病原压力）。这些机制共同塑造了基因组的动态性和生物多样性。

---

### 8. 比较基因组学资源（Ensembl、UCSC Genome Browser）的功能与应用

比较基因组学的重要性
- 多次强调通过跨物种基因组比较来解析基因的起源、功能演化和形态创新（如基因重复、水平转移、调控区演化）。例如：
	- ​**基因家族扩张**：人类唾液淀粉酶基因（AMY1）的串联重复适应高淀粉饮食（文档3）。
	- ​**同源基因分析**：Hox基因在脊椎动物和无脊椎动物中的保守性与功能分化（文档1、5）。
	- ​**新基因起源**：蚜虫通过水平基因转移获得真菌的类胡萝卜素合成基因（文档3）。
- 这些研究依赖于基因组数据的整合、可视化和多物种比对，而**Ensembl**和**UCSC Genome Browser**是两大核心工具。

 Ensembl的功能与适用场景
- **核心功能**：
	1. ​**基因注释与结构分析**：
	    - 提供基因位置、外显子-内含子结构、可变剪接等信息。
	    - ​**案例**：分析Hox基因的跨物种保守性（文档1），验证其在不同动物中的外显子结构。
	2. ​**比较基因组学工具**：
	    - ​**基因树（Gene Tree）​**：追踪基因家族演化历史，识别旁系同源（Paralog）和直系同源（Ortholog）。
	    - ​**案例**：研究抗冻蛋白基因的外显子洗牌事件（文档3）。
	3. ​**变异数据库**：
	    - 整合SNP、CNV等变异数据，支持功能预测。
	    - ​**案例**：分析CCR5Δ32缺失突变的功能影响（文档3）。
	4. ​**调控元件注释**：
	    - 标注启动子、增强子等非编码调控区域。
	    - ​**案例**：研究MYH16基因调控区缺失对咀嚼肌退化的影响（文档3）。
- **优势**：
	- 适用于大规模基因家族分析、进化树构建和跨物种功能保守性研究。

UCSC Genome Browser的功能与适用场景
- **核心功能**：
	1. ​**多轨道可视化**：
	    - 叠加基因注释、保守性评分（PhastCons/PhyloP）、表观遗传数据（如ChIP-seq、DNA甲基化）。
	    - ​**案例**：识别刺突蛋白（SARS-CoV-2）重组区域（文档3）。
	2. ​**多物种比对**：
	    - 支持100+物种的基因组比对，直观显示同源区域。
	    - ​**案例**：分析Distal-less基因调控区在蝴蝶眼点演化中的趋同变化（文档1）。
	3. ​**自定义数据整合**：
	    - 用户可上传RNA-seq、ATAC-seq等数据与公共数据对比。
	    - ​**案例**：验证新基因（如XIST）在X染色体失活中的表达模式（文档3）。
	4. ​**保守性分析工具**：
	    - 通过PhastCons和PhyloP评估序列保守性，定位功能关键区域。
	    - ​**案例**：研究Hedgehog信号通路调控区的阈值效应（文档1）。
- **优势**：
	- 适合精细调控分析、序列保守性研究和多组学数据整合。

工具对比与协同使用：

|​**功能**|​**Ensembl**|​**UCSC Genome Browser**|
|---|---|---|
|​**核心应用**|基因家族演化、变异数据库、功能注释|多轨道可视化、保守性分析、自定义数据整合|
|​**多物种比对**|支持Gene Tree和同源基因检索|提供PhastCons/PhyloP轨道和多物种视图|
|​**调控分析**|启动子/增强子标注|表观遗传数据叠加（如组蛋白修饰）|
|​**案例场景**|AMY1基因重复分析（文档3）|刺突蛋白重组区域可视化（文档3）|

**协同策略**：
- 使用Ensembl进行基因家族演化和功能注释，再通过UCSC Genome Browser深入分析调控机制和保守性。

文档中的具体应用示例：
1. ​**Hox基因的同源性与功能分化**​（文档1、5）：
    - ​**Ensembl**：构建Hox基因家族树，识别直系同源基因（如果蝇Antennapedia与小鼠HoxB6）。
    - ​**UCSC**：通过PhastCons轨道分析Hox基因调控区的保守性，揭示跨物种的发育调控机制。
2. ​**新基因起源研究**​（文档3）：
    - ​**Ensembl**：分析蚜虫类胡萝卜素基因的水平转移事件，比对真菌与蚜虫基因组。
    - ​**UCSC**：上传自定义RNA-seq数据，验证新基因在体色发育中的表达。
3. ​**结构变异与适应性演化**​（文档3）：
    - ​**Ensembl**：检索AMY1基因的拷贝数变异（CNV）数据库。
    - ​**UCSC**：通过CNV轨道可视化不同人群的AMY1拷贝数分布。

总结：Ensembl和UCSC Genome Browser是互补的比较基因组学工具
- ​**Ensembl** 强于基因注释、家族演化和变异分析，适合理论驱动的假设验证。
- ​**UCSC** 长于多维度数据可视化和保守性解析，支持探索性研究和复杂调控网络分析。  
    两者结合，可全面解析从序列演化到表型创新的生物学机制，如文档中提到的基因重复、水平转移和调控区演化。


# 陈华老师部分

#### ​**1. 哈迪-温伯格平衡（HW平衡）​**

- ​**条件**：随机交配、大群体、无突变、迁移、选择、两性等位基因频率相同。
- ​**基因型频率**： $\text{AA: } p^2, \quad \text{Aa: } 2pq, \quad \text{aa: } q^2$
- ​**验证方法**：卡方检验（比较观测与预期基因型频率）。

在一个大且随机交配的种群中，若没有突变、迁移、选择、遗传漂变等因素的干扰，基因频率和基因型频率在世代之间会保持不变，这种状态就称为哈代-温伯格平衡。

对于一个基因的两种等位基因A和a，其频率分别为p和q，满足p+q=1。根据哈代-温伯格定律，三种基因型AA、Aa、aa的频率分别为p²、2pq和q²，且p²+2pq+q²=1。

前提条件：种群无限大、种群内个体间随机交配、没有突变、没有自然选择、没有大规模的迁移、没有遗传漂变、没有近亲交配。

---

#### ​**2. 遗传漂变与杂合度衰减规律**

- ​**公式**：杂合度 $\mathcal{H}_t = \mathcal{H}_0 \left(1 - \frac{1}{2N}\right)^t$，其中 N 为有效群体大小。
- ​**意义**：小群体中漂变更强，杂合度随世代指数衰减。

遗传漂变是指在小种群中，由于随机因素（如个体的随机生存、繁殖、死亡等）导致基因频率发生随机变化的现象。这种变化是随机的，不受自然选择、突变等因素的直接影响。

---

#### ​**3. 群体迁移、近交系数、Fst、Wahlund定律**

- ​**近交系数（F）​**：衡量群体内近交程度，$F = \frac{H_0 - H}{H_0}​$，$H_0 = 2pq$ 为 HW 平衡杂合度。
- ​**群体分化指数（Fst）​**： $F_{ST} = \frac{\sigma^2}{\bar{p}\bar{q}} \quad (\sigma^2 \text{为亚群等位基因频率方差})$
- ​**岛屿模型**：平衡时 $F_{ST} = \frac{1}{4Nm + 1}​$，迁移率 m 高或群体大 NNN 时分化低。
- ​**Wahlund定律**：混合群体杂合度低于各亚群平均值（$H_S < H_T$​），因亚群分化导致纯合子过剩。

群体迁移：指生物个体或群体从一个地理区域移动到另一个地理区域的现象。
- 在群体遗传学中，群体迁移会导致基因流动，即不同群体之间的基因交流。
- 这种基因流动可以增加群体的遗传多样性，减少遗传分化，对种群的进化和适应性有重要影响。

近交系数：衡量一个个体在某基因座位上从父母双方继承的等位基因是同源（即从共同祖先继承）的概率。
- 它反映了个体的父母是否有血缘关系及其程度，从而表示个体的近亲交配程度

Fst：衡量群体间遗传分化程度的指标。
- 它基于群体的SNP数据来估计，反映了群体结构可以解释的遗传变异的量。
- Fst的值介于0到1之间，越接近1表示群体间的分化程度越高。

Wahlund定律：在一个由多个亚群体组成的群体中，如果亚群体之间存在遗传分化，那么整个群体的杂合度会低于各亚群体杂合度的加权平均值。
- 这表明群体结构会影响群体的遗传多样性，亚群体间的遗传分化会导致群体整体的杂合度降低

**假设两个亚群**：

- 亚群1：p1=0.2p_1 = 0.2p1​=0.2，杂合度 H1=2⋅0.2⋅0.8=0.32H_1 = 2 \cdot 0.2 \cdot 0.8 = 0.32H1​=2⋅0.2⋅0.8=0.32
- 亚群2：p2=0.8p_2 = 0.8p2​=0.8，杂合度 H2=2⋅0.8⋅0.2=0.32H_2 = 2 \cdot 0.8 \cdot 0.2 = 0.32H2​=2⋅0.8⋅0.2=0.32

**计算总群体参数**：

- 平均等位基因频率：$\bar{p} = \frac{0.2 + 0.8}{2} = 0.5$
- 预期总杂合度：$H_{\text{预期总群体}} = 2 \cdot 0.5 \cdot 0.5 = 0.5$
- 亚群间方差：$\text{Var}(p) = \frac{(0.2 - 0.5)^2 + (0.8 - 0.5)^2}{2} = 0.09$
- 平均亚群内杂合度：$\frac{0.32 + 0.32}{2} = 0.32$

**验证公式**：

$0.32 = 0.5 - 2 \cdot 0.09 \quad \Rightarrow \quad 0.32 = 0.5 - 0.18 \quad \text{成立。}$

---

#### ​**4. 遗传多态性的类型**

- ​**常见类型**：SNP、STR（短串联重复）、RFLP（限制性片段长度多态）、SV（结构变异）、CNV（拷贝数变异）。
- Haplotype 单倍型
- LD
- 等位基因频谱

---

#### ​**5. 等位基因频谱（AFS）与单倍型结构**

- ​**AFS**：描述等位基因频率分布（如低频变异占比高提示净化选择）。
- ​**单倍型结构**：
    - ​**EHH（扩展单倍型纯合度）​**：检测长单倍型区块（正选择区域衰减慢）。
    - ​**iHS**：比较祖先与衍生等位基因的单倍型积分差异。

等位基因频谱：群体遗传学中的一个重要概念，用来显示一个种群中特定基因座上各个等位基因所占的频率，或者说是等位基因在基因库中的丰富程度。
- 它可以帮助研究者了解基因频率的分布情况，从而推断种群的进化历史、遗传多样性和自然选择等。

单倍型结构：单倍型（Haplotype）是指在同一染色体上紧密连锁的多个基因座上等位基因的组合。
- 单倍型结构反映了等位基因的连锁遗传关系。在减数分裂过程中，位于同一条染色体上的等位基因倾向于一起遗传，形成特定的单倍型传递给子代。
- 这种连锁遗传使得单倍型在世代传递中保持相对稳定，除非发生重组等遗传事件
- 表现形式：
	- 柱状图，横坐标是每个SNP衍生等位基因数，纵坐标这种类型SNP的数目。
	- 多个snp的联合

---

#### ​**6. 溯祖过程（Coalescent）​**

- ​**概念**：追溯样本序列的最近共同祖先（MRCA）。
- ​**两条序列**：合并时间 $T_2$​ 服从几何分布 $P(T_2=j) = \left(1-\frac{1}{2N}\right)^{j-1}\frac{1}{2N}$​。
- ​**多条序列**：逐步合并，第 k 条合并时间期望 $E[T_k] = \frac{4N}{k(k-1)}​$。

溯祖过程（Coalescent Process） 是一种群体遗传学模型，用于研究样本基因序列在回溯过程中找到共同祖先的分布。
- 主要特点：
	1. 回溯时间：溯祖过程关注的是样本在回溯过程中何时找到共同祖先（Most Recent Common Ancestor, MRCA）。
	2. 随机性：溯祖事件的发生是随机的，每一代中任意两条序列合并的概率为1/2N，其中 N 是有效群体大小。
	3. 指数分布：两次溯祖事件之间的等待时间满足指数分布，其均值为 2N 代。

两条序列的溯祖过程：假设从一个满足Fisher-Wright模型的群体中随机抽取两条序列，它们必定来自某个最近的共同祖先（MRCA）。我们可以通过以下步骤分析它们的溯祖过程：
1. 合并概率：
	- 在上一代中，两条序列合并的概率为1/2N。
	- 在上一代中不合并的概率为 1-1/2N。
2. 等待时间：
	- 两条序列完成溯祖合并的等待时间 T 满足几何分布，其均值为 2N 代。
	- 如果用突变率μ来衡量等待时间，那么等待时间的均值为1/μ，其中μ是每世代每位点的突变率。
3. 突变积累：
	- 从MRCA到当前代，每条序列在每个位点上平均积累的突变数为 2Nμ。
	- 两条序列之间的平均突变数为 4Nμ，这反映了它们之间的遗传距离。
4. 群体大小参数：群体大小参数 θ=4Nμ 是群体遗传多样性的度量指标，反映了突变引入遗传变异与遗传漂变降低多态性之间的平衡
	- 共祖理论是向时间上追溯样本族谱时连接谱系的过程
		- 当两个谱系被追踪到一个共同事件时，称为一个共祖事件。
		- 所有现存样本的单一祖先被称为最近公共祖先或MRCA。
	- 两条序列溯祖概率p=1/2N

---

#### ​**7. 谱系树参数计算**

- ​**树高度**：所有合并时间之和 $T_{\text{height}} = \sum_{i=2}^n T_i$​。
	- 谱系树的高度通常指的是从最近的共同祖先（MRCA）到最远的后代之间的最大距离。
	- 在群体遗传学中，谱系树的高度可以通过计算TMRCA来间接表示。
- ​**TMRCA（最近共同祖先时间）​**：树高度。
- ​**总枝长（TBL）​**：支长总和 $\sum_{k=2}^n kT_k$​，反映总突变量。

---

#### ​**8. Tajima's D、Watterson θ_w、π 计算**

- ​**Watterson θ_w**：基于分离位点数 S，$\theta_w = \frac{S}{\sum_{i=1}^{n-1} \frac{1}{i}}$​。
- ​**核苷酸多样性（π）​**：平均两序列差异，$\pi = \frac{\sum_{i<j} d_{ij}}{\binom{n}{2}}$​​。
- ​**Tajima's D**： $D = \frac{\pi - \theta_w}{\sqrt{\text{Var}(\pi - \theta_w)}}$
    - D > 0：低频变异缺失（平衡选择或群体收缩）。
    - D < 0：高频变异缺失（正选择或群体扩张）。

---

#### ​**9. 群体历史推断方法**

- ​**单群体**：PSMC（利用基因组重组断点推断有效群体大小变化）。
- ​**多群体**：dadi（联合等位基因频谱）、MSMC（多样本溯祖模型）。
- ​**工具**：G-PhoCS（贝叶斯框架下推断分化时间与基因流）。

单群体
1. PSMC（两条序列-LD-突变的数目反映时间，Tmrca）
	- 基于两条序列（二倍体个体的单条染色体）的基因组比对，利用重组（LD）和突变信息，通过隐马尔可夫模型（HMM）推断历史上不同时间的Ne变化。
2. 等位基因频谱（marth种群大小持续时间、polanski指数模型初始大小，增长率，增长时间）
	- 分析群体中突变频率分布（如 SNP 频谱），推断历史群体大小变化。

多群体
1. MSMC（多条序列）
	- PSMC 的扩展，利用多个个体（通常 4-8 条单倍型）的基因组，通过跨群体的共祖事件（coalescence）推断：分化时间（如人类与尼安德特人分离时间）、基因流（如古代混合事件）。
2. 联合等位基因频谱
	- 比较两个或多个群体的等位基因频率联合分布，推断：分化时间（如非洲 vs. 非非洲群体）、祖先群体大小（如走出非洲前的Ne）、基因流方向（如农业扩张中的混合信号）。

---

#### ​**10. 自然选择的类型**

- ​**正选择**：有利突变扩散（如硬扫描、软扫描）。
	- 某一等位基因因提供生存或繁殖优势而被选择保留，导致其在群体中频率上升。
- ​**负选择**：清除有害突变。
	- 有害突变被选择清除，维持功能基因的保守性。
- ​**平衡选择**：维持多态（如杂合子优势）。
	- 维持多个等位基因在群体中的稳定共存，避免单一等位基因固定。
- ​**背景选择**：连锁有害突变导致中性位点多态性降低。
	- 基因组中受负选择区域通过连锁效应（LD）清除周围中性突变，降低局部多样性。
- 便车效应：中性或轻微有害突变因与受正选择的突变连锁而被一起固定或清除。

---

#### ​**11. Hard Sweep vs. Soft Sweep**

- ​**Hard Sweep**：单一新突变快速固定，单倍型区块长。
	- 指单个新出现的有利突变在群体中快速固定，导致附近连锁的中性突变（通过便车效应）也被固定或清除，从而显著降低局部遗传多样性。
	- 通常发生在大群体中，且有利突变最初频率极低（如全新突变）。
- ​**Soft Sweep**：已有多态或多次突变被选择，单倍型多样性高。
	- 指多个独立的有利突变（或已有变异）因选择压力同时上升频率，导致群体中多种单倍型携带有利等位基因，局部多样性部分保留。
	- 通常发生在群体已有遗传变异（如多态性位点中部分等位基因突然变得有利）、小群体或频繁基因流环境中。

比较：
- Hard sweep强调了单个新突变的快速固定，而Soft sweep则强调了已有变异的利用和多次独立突变的可能性。
- 软性选择：
	- Soft sweep描述的是多个携带适应性等位基因的单倍型在群体中上升到高频率的过程，这些单倍型可能在适应性事件发生之前就已经存在。
	- 与Hard sweep相比，Soft sweep在群体遗传结构上留下的痕迹较为微妙，可能更难通过传统的选择信号检测方法发现。
	- Soft sweep可能与温和的选择压力、群体的遗传多样性以及种群结构的特点（如亚群间的基因流）有关
- 硬性选择：Hard sweep通常指的是一个新的有益突变在群体中出现，并且迅速增加频率直至固定的过程。
- 在Hard sweep过程中，与该有益突变位点连锁的单倍型也会随之增加频率并最终固定，导致该位点周围区域的遗传多样性减少。
	- 这种选择事件在基因组上留下了明显的印记，即所谓的选择信号，可以通过统计测试（如Tajima's D或HKA测试）来检测。
- Hard sweep通常与快速适应和强烈的自然选择压力相关联。
- Hard sweep强调了单个新突变的快速固定，而Soft sweep则强调了已有变异的利用和多次独立突变的可能性。
	- 这两种模型在解释遗传数据和理解适应性演化过程中都是重要的工具


---

#### ​**12. Hitchhiking Effect（搭便车效应）​**

- ​**定义**：中性位点因与选择位点连锁而频率变化（正选择降低多态性，背景选择清除变异）。

便车效应是指基因组中中性或轻微有害的突变因与受强烈正选择的有利突变物理连锁（位于同一染色体区域且重组率低），而在群体中频率被动上升或下降的现象。它是自然选择影响基因组多样性的重要机制之一。
- 核心机制
	- 连锁不平衡（LD）：当有利突变被选择时，其周围一定范围内的中性突变会因缺乏足够时间被重组分开而“搭便车”。
- 选择强度与范围：选择越强，清除区域越大（如硬清除可影响数百kb）。重组率越低，便车效应越显著（如着丝粒附近区域）。
- 两种主要类型：
	1. 选择性清除（Selective Sweep）
		- 硬清除（Hard Sweep）：单一有利突变连带清除周围变异，导致局部多样性骤降（经典便车效应）。
		- 软清除（Soft Sweep）：多个有利突变独立出现，多样性部分保留（便车效应较弱）。
	2. 背景选择（Background Selection）
		- 有害突变被负选择清除时，连带清除周围中性突变，降低局部多样性。


---

#### ​**13. 检测自然选择的遗传多态性**

- ​**类型**：SNP（等位频率）、单倍型（长度与结构）、连锁不平衡（LD）。
	- SNP-等位基因频谱
	- 单倍型-LD
- 单核苷酸多态性、微卫星（Microsatellites）或短串联重复（STRs, Short Tandem Repeats）、拷贝数变异、结构变异、单倍型、转座元件。

---

#### ​**14. 自然选择检测方法及原理**

- ​**Tajima's D**：基于等位频谱偏离中性预期。
- ​**EHH/iHS**：长单倍型提示近期正选择。
- ​**XP-EHH**：跨群体比较单倍型纯合度。
- ​**MK检验**：比较种内多态与种间分歧的同义/非同义突变比例。

一、种内自然选择检测（Intra-specific Selection）
1. 基于等位基因频率的方法
	- Tajima's D 检验
		- 原理：比较突变数量（θ）与配对差异（π）的偏离。
		- 正选择：Tajima's D < 0（低频突变富集，提示近期选择清除）。
		- 平衡选择：Tajima's D > 0（高频突变过多，维持多态性）。
		- 适用场景：全基因组扫描选择信号。
	- FST（群体分化指数）
		- 原理：量化群体间等位基因频率差异。
		- 局限：需排除群体结构（如隔离）的干扰。
	- 等位基因频谱（AFS）分析
		- 原理：拟合观测频谱与模型（如扩张、瓶颈、选择），推断历史选择事件。
2. 基于单倍型的方法
	- iHS（Integrated Haplotype Score）
		- 原理：检测未完成清除的长单倍型（常见于近期正选择）。
	- XP-EHH（Cross-population Extended Haplotype Homozygosity）
		- 原理：比较两群体的单倍型延伸程度，识别某一群体中的选择信号。
3. 基于功能变异的分析
	- dN/dS 比率
		- 原理：比较非同义突变（dN）与同义突变（dS）频率。
			- dN/dS > 1：正选择。
			- dN/dS < 1：负选择。
		- 局限：仅适用于编码区。

二、种间自然选择检测（Inter-specific Selection）
1. dN/dS 比率
	- 原理：比较跨物种同源基因的dN/dS：
		- dN/dS > 1：正选择（如灵长类TRIM5α抗病毒基因）。
		- dN/dS ≈ 1：中性进化。
		- dN/dS < 1：负选择。
2. Ka/Ks 比率
	- Ka：非同义替换率；Ks：同义替换率。
3. MK test
	- 一种用于检测自然选择的经典方法，通过比较种内多态性（Polymorphism）和种间分化（Divergence）在同义突变（synonymous）和非同义突变（non-synonymous）上的比例，来判断基因是否受到选择作用。
	- 其核心逻辑是：
		- 中性进化假设下，同义突变和非同义突变的种内多态性（P）与种间分化（D）的比例应相等。
		- 若比例显著偏离，则表明存在自然选择。

---

#### ​**15. MK检验计算**

- ​**步骤**：
    1. ​**构建2×2表格**：
        ||同义突变|非同义突变|
        |---|---|---|
        |种内多态|S_p​|N_p​|
        |种间分歧|S_d​|N_d​|
    2. ​**计算期望值**：假设中性演化下同义/非同义比例一致。
    3. ​**卡方检验**： $\chi^2 = \sum \frac{(O-E)^2}{E}$
    4. ​**结论**：若 $N_d/S_d > N_p/S_p$​，提示正选择；反之提示净化选择。


# 钱文峰老师部分

钱老师PPT：
- Class 1: https://prezi.com/view/O151s2egrPmGEpl4Esgs/
- Class 2: https://prezi.com/view/nIZZgXUWbyyh8bu2vLK2/
- Class 3: https://prezi.com/view/0R722VcUcqfQtlBMwfh9/
- Class 4: https://prezi.com/view/E4WsNAFCorFqIFY5u4VQ/

# 讨论课作业

曼哈顿图是怎么做出来的，和一般GWAS有什么区别？是找特殊SDS相应的SNP吗

SNP、rare allele、singleton 有什么区别？

SDS相对于iHS有没有什么坏处？有没有可能综合起来用？

result部分讲的时候可以根据摘要里面分成的几个点。
