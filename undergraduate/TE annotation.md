work list:
1. 转座子插入时间：特别是LTR
	1. 计算并画出图像
2. Chinese Spring的转座子分析文章
	1. 根据其转座子分析套路、代码，得到对转座子分布的目的工作
	2. 向钮师姐请教转座子分析pipeline中所使用的软件和方法
3. *Copia*, *Gsypy*两种转座子容易聚集在着丝粒位点附近的原因
	1. 根据燕麦和水稻3以及KN做的比较好的着丝粒重复位点分析来进行
		1. TE
		2. 串联重复序列 (tandom repeat sequence)

# Insertion time/age

calculation: insertion time $T=\frac{K}{2\mu}$
- $K$: Gene distance
- $\mu$: Substitution rate

# TE component

## knowing data

Supplementary Figure 14: distribution of TE on different chrosomes

Supplementary Figure 17: TE proportion on different subgenome

JM
- Copia: 
	- reference Copia: 788,489
	- **-w "Copia": 1,125,250**
		- **homology: 724,344**
			- -w "Copia_LTR_retrotransposon": 724,344
			- ID: TE_homo_
		- structural: 400,906
			- **Parent: 334,073**
				- -w "Copia_LTR_retrotransposon": 66,833
					- -w '?': 634
				- -w "long_terminal_repeat": 133,666
					- -w '?': 1,268
				- -w "target_site_duplication": 133,574
					- -w '?': 1,268
			- **-w "repeat_region": 66,833**
				- including all of the parent
				- -w '?': 634
				- ID: repeat_region_
		- sum(homology ,real_structural) = 791,177
			- difference: 2,688
- all: 8559935
	- ID: 7,460,637 (without Parent)
		- **TE_homo_**: 7,101,886
			- == homology
		- **repeat_region_**: 219,924
			- **Parent**: 1,099,298
				- "TR_retrotransposon": 219,924
					- LTRRT_: 219,924
				- "long_terminal_repeat": 439848
					- lLTR_: 219,924
					- rLTR_: 219,924
				- "target_site_duplication": 439526
					- lTSD_: 219,763
					- rTSD_: 219,763
		- **TIR**: 123,436
		- **helitron**: 15,391

- Long Terminal Repeats (LTRs)
- Target Site Repeats (TSRs)
- Primer Binding Sites (PBSs)
- Polypurine Tract (PPT)
- TG ...CA box
- sites of 
	- Reverse Transcriptase (RT)
	- Integrase (IN)
	- RNaseH (RH)

## pipeline

The Extensive _de novo_ TE Annotator (EDTA)

# Centromeres sequence analysis

Supplementary Table10: The position of centromeres on chromosomes

there is a saying that LTR retroTE may play a important role in the evolution of plant genome size
- polyploidy: maybe some factor of genome was diluted and its relgularly distribute on the genome in a rule, or, its a gene that have been discovered