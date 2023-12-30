# Basic

## reference genome:

Wheat species:
 - AA:
	 - *T. monococcum* L. ssp.
		 - *boeoticum* Boiss. : *T. boeoticum* (wild einkorn)
		 - *monococcum*: *T. monococcum* (cultivated einkorn)
	 - *T. urartu* Tuman. : *T. urartu* (wild *T. urartu*)
 - DD:
	 - *Ae. tauschii* Coss. : *Ae. tauschii* (wild *Ae. Tauschii*)
 - AABB:
	 - *T. turgidum* L. ssp.
		 - *dicoccoides* Aschers: *T. dicoccoides* (wild emmer)
		 - *dicoccum* Schubl. : *T. dicoccum* (cultivated emmer)
		 - *durum* Desf. : *T. durum* (hard wheat)
		 - *parvicoccum* Kislev: *T. parvicoccum* (*T. parvicoccum*, archaeobotanical)
 - AABBDD:
	 - *T. aestivum* L. ssp. 
		 - *spelta*: *T. spelta* (spelt)
		 - *vulgare* Host: *T. vulgare* (bread wheat)

![[GeneticsNotes/undergraduate/Data.xlsx]]

models for the evolution of polyploid wheats
 1. wild emmer -> cultivated emmer
 2. cultivated emmer -> *T. durum* & *T. turgidum* (*T. parvicoccum*)
 3. with wild *Ae. tauschii*
	 - cultivated emmer -> *T. spelta*
	 - *T. durum* & *T. parvicoccum* -> *T. vulgare*
 4. transform:
	 - *T. spelta* -> *T. vulgare*
	 - *T. vulgare* with cultivated emmer -> *T. spelta*

## Transposable Element (TE)

types:
- DNA (mite, etc)
- LTR (gypsy, etc)

## re-sequencing data: Vmap 2

重测序数据：VMap 2 (>1000 accession)
1. Fastq
2. random selection: 10,000 reads
3. TE, blast

## TE library

| TE\Wheat | a1  | a2  | a3  | ... |
| -------- | --- | --- | --- | --- |
| T1       |     |     |     |     |
| T2       |     |     |     |     |
| T3       |     |     |     |     |
| ...      |     |     |     |     |

# Practice

## data preparing

conda problem:
1. mamba can not work
	1. figure out in the file: failed
2. uninstall conda and memba

research
1. reviews of transposable element and tools to discover them

## TE detection in genomes

categories:
- *de novo*
- Structure
- Comparative Genomic
- Homology-based

detection tools:
- BLAT
- Censor
- LTR Finder
- PILER
- Repeat Masker
- INSurVeyor
- RepeatModeler2
- TIR-Learner

## reads mapping

二代测序：原理、reads长度、文件存储数据、二代分析测序流程
- 长度为几百bp：限制条件，也因此必须了解目标序列（转座子）的长度

将reads比对到基因组上的工具：bwa (bowtie2, or else)

## Population

群体分型 (population stratification)：是GWAS等方式的基础

