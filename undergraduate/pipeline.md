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

Vmap 2 数据包括：
- vcf文件：只包含了SNP位点/片段的reads比对到reference上
	- 也就是每个样本相对于reference的突变性
- bam文件：reads比对到reference上

## TE library

| TE\Wheat | a1  | a2  | a3  | ... |
| -------- | --- | --- | --- | --- |
| T1       |     |     |     |     |
| T2       |     |     |     |     |
| T3       |     |     |     |     |
| ...      |     |     |     |     |

# Reference



# Practice

## data preparing

conda problem:
1. mamba can not work
	1. figure out in the file: failed
2. uninstall conda and memba

research
1. reviews of transposable element and tools to discover them

reference genome:
- Chinese Spring

## TE detection in reference genomes

categories:
- *de novo*
- Structure
- Comparative Genomic
- Homology-based

machine learning: which I was familiar to
- decision tree: 
	- ID3 (Iterative Dichotomister 3) algorithm
	- C4.5 algorithm
- association rule learning
- artificial neural networks
- inductive logic programming
- support vector machines
- Bayesian network

performance evaluation:
- accuracy
- precision
- recall
- F-measure

detection tools:
- BLAT
- Censor
- LTR Finder
- PILER
- Repeat Masker
- INSurVeyor
- RepeatModeler2
- TIR-Learner

评判标准：
- of different TE

Chinese Spring 转座子库文件格式：RepeatMasker -> CLARI-TE
```
//1. xm output file from RepeatMasker
1725 20.7 2.6 0.8 v443_2791 5 393 (40687) C ctgB_rep_0246#Unknown (7481) 396 1 * 
4791 21.8 0.8 3.3 v443_2791 378 1704 (39376) + ctgF_rep_0077#Unknown 322 1615 (7557) * 
5649 11.4 0.4 0.4 v443_2791 799 1704 (39376) + ctgF_rep_0055#Unknown 722 1627 (11086) 
15719 9.1 0.5 0.7 v443_2791 6858 9147 (31933) + ctgF_rep_0055#Unknown 5829 8115 (4598) 
9263 22.2 0.9 2.8 v443_2791 7600 9932 (31148) + ctgF_rep_0077#Unknown 2241 4528 (4644) *

//2. tabular file of the classification
#sequenceID family 
	TREP100 RLC_famc1.1 
	TREP1000 DTT_famn14 
	TREP1001 DTT_famn1

//3. Tabular file of the position of LTR in the LTR retrotransposons Note
#sequenceID family 
	LTRtype start end 
	ctgH_rep_0307 RLG_famc3 LTR5 1 3945 
	ctgH_rep_0307 RLG_famc3 LTR3 7931 12091 
	sr2_rep_0226 RLC_famc9 LTR5 1 214 
	sr2_rep_0226 RLC_famc9 LTR3 4972 5185

//4. Gene annotation in EMBL format TriAnnot Note
ID unknown; SV 1; linear; unassigned DNA; STD; UNC; 1411106 BP. XX AC unknown; XX XX 
	FT CDS join(141960..142006,142121..142147,142248..142370,142493..142739,142850..142873) 
	FT /locus_tag="v443_0002_EXONERATE_BLASTX_protOSA_6" 
	FT /blastp_file="v443_0002_EXONERATE_BLASTX_protOSA_141960_142873_Q5JM42_Match_0005_mRNA_CDS.bltp" 
	FT /id="v443_0002_EXONERATE_BLASTX_protOSA_141960_142873_Q5JM42_Match_0005_mRNA_joinedCDS" 
	FT /note="Similar_to: hypothetical_protein" 
	FT /note="BestBlastHit: B9EZI3_ORYSJ TrEMBL databank Putative uncharacterized protein - %25id: 91.67 - hcov: 13.78 - qcov: 100.00" 
	FT /note="Status: High Confidence" 
	
	FT CDS complement(join(143435..144154,144239..144363,145030..145267)) 
	FT /locus_tag="v443_0002_EXONERATE_BLASTX_validated_9" 
	FT /expressed 
	FT /blastp_file="v443_0002_EXONERATE_BLASTX_validated_143435_145267_AFR_02_CAT01_3_Match_0001_mRNA_CDS.bltp" 
	FT /id="v443_0002_EXONERATE_BLASTX_validated_143435_145267_AFR_02_CAT01_3_Match_0001_mRNA_joinedCDS" 
	FT /note="Similar_to: putative_function - F2CSA4_HORVD TrEMBL databank Predicted protein OS Hordeum vulgare var distichum PE 2 SV 1" 
	FT /note="BestBlastHit: F2CSA4_HORVD TrEMBL databank Predicted protein - %25id: 96.12 - hcov: 100.56 - qcov: 100.00" 
	FT /note="Function_coverage: 94.71" 
	FT /note="Function_identity: 97.94" 
	FT /note="Function_target: F2CSA4 22 361" 
	FT /note="Status: High Confidence"

//Output
ID unknown; SV 1; linear; unassigned DNA; STD; UNC; 1411106 BP. XX AC unknown; XX XX 
	FH Key Location/Qualifiers FH FT repeat_region complement(join(10..373,1824..2754)) 
	FT /parent="mp1" # parent id 
	FT /status="fragmented" # status of the predicton (complete or fragmented) 
	FT /range="3854..4785,4881..5242," # position on the reference sequence used to annotated the prediction 
	FT /post="RLG_famc36 8671bp 3854..5242" # tag 
	FT /compo="RLG_famc36 100.00 " # composition of the prediction 
	FT /id="3_v443_0001" # id of the prediction 
	FT /copie="ctgD_rep_0264" # sequenceID in the library used to annotated the prediction

//Actual output, gff3
chr1A   CLARITE_CLARIrepeatwheat        repeat_region   77568   86766   .       -       .       
// attributes: 
	ID=scaffold38755_chunk_1_CLARITE_CLARIrepeatwheat_77568_86766_Repeat_region_1;
	Name=CLARITE_CLARIrepeatwheat_77568_86766_Repeat_region_1;
	Ontology_term=SO:0000657;
	compo=RLG_famc1.4 82.30 RLG_famc1.1 4.69 RLG_famc1.2 12.61 no_match 0.40;
	status=complete
```

RepeatMasker:
- The output of the program is 
	- a detailed annotation of the repeats that are present in the query sequence
	- a modified version of the query sequence in which all the annotated repeats have been masked (default: replaced by Ns).

提取转座子位点工具：SeqKit v2.6.1
```
\\move chr1A to certain file 
cat iwgsc_refseqv1.0_TransposableElements_2017Mar13.gff3 | grep -w 'chr1A' > chr1A/chr1A.gff3
seqkit grep -p 1 abd_iwgscV1.fa -o chr1A/chr1A1.fa

seqkit stats 
```

序列合并工具：Seqtk v1.4

check the exiting TE types in the TE annotation of reference genome CSv1.0
1. extract TE types in the gff3 annotation file (attributes), python
```
# Open the GFF3 file for reading
with open('iwgsc_refseqv1.0_TransposableElements_2017Mar13.gff3', 'r') as gff_file:
    # Initialize a dictionary to store category counts
    category_counts = {}

    # Iterate through each line in the file
    for line in gff_file:
        # Skip comment lines starting with #
        if line.startswith('#'):
            continue

        # Split the line into fields
        fields = line.strip().split('\t')

        # Check if the line has enough fields
        if len(fields) >= 9:
            # Extract the attributes field
            attributes = fields[8]

            # Split the attributes field into key-value pairs
            attribute_pairs = [pair.split('=') for pair in attributes.split(';')]

            # Extract the category/type from the attribute pairs
            for key, value in attribute_pairs:
                if key == 'compo':
                    category = value
                    break
            else:
                # If 'Type' is not found, use the last key-value pair
                category = attribute_pairs[-1][0]

            # Update the category count in the dictionary
            category_counts[category] = category_counts.get(category, 0) + 1

# Print the category counts
for category, count in category_counts.items():
    print(f'{category}: {count}')
```
2. `python de.py > tte.gff3`
3. `grep -E -o 'DTA|DTB|DTC|DTE|DTH|DTM|DTP|DTR|DTT|DTX|DYC|DHH|DMM|DXX|RLC|RLG|RLB|RLR|RLE|RLX|RYD|RYN|RYV|RPP|RIR|RIT|RIJ|RIL|RII|RIX|RST|RSL|RSS|RSX|RXX|XXX' tte.gff3 | sort -u > check.gff3`

analysis by perl code

## reads mapping

二代测序：原理、reads长度、文件存储数据、二代分析测序流程
- 长度为几百bp：限制条件，也因此必须了解目标序列（转座子）的长度

将reads比对到基因组上的工具：bwa (bowtie2, or else)
- 目前已经有bam文件，无需继续计算

## Population

群体分型 (population stratification)：是GWAS等方式的基础

后面再学习，先将现在的工作做好

DTA|DTB|DTC|DTE|DTH|DTM|DTP|DTR|DTT|DTX|DYC|DHH|DMM|DXX|RLC|RLG|RLB|RLR|RLE|RLX|RYD|RYN|RYV|RPP|RIR|RIT|RIJ|RIL|RII|RIX|RST|RSL|RSS|RSX|RXX|XXX