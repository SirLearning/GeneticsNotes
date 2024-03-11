# outside

![[GeneticsNotes/undergraduate/files/Data.xlsx]]
![[Presentation.pptx]]
# TE detect

用长reads，有空间位点的信息，可以直接检测
- 长reads的检测工具

## Reference genome (data 1)

Why reference: The genome has the sequence of the whole specie's genetic information. But why we should put a reference genome as a reference?
- For technology: 
	- different sequences have sequenced by different sequencing technology, the most precise one is the reference
	- no, the chinese spring didn't have a great result 
- For alignment anchor: alignment sequences from different genome needs one as the basic anchor to decide whether there is a change or not

当前只用找到这个地步，先把一个abd的跑通再说其他种类的小麦
长读段同样，目前123的数据足以使用

由于abd的长度很长，选择其中的chr1A的一小段

## TE library (data 2)

TE library: the reliable TE and sequence for one species
- existing manual curative TE library: the proved reliable TE library, the basis of TE detect tools
	- TREP
	- Dfam: repetitive families
	- Repbase: repbase 2018 (github)
- how to build curated library: "A beginner’s guide to manual curation of transposable elements"

## TE detection (data 3)

categories:
- *de novo*
- Structure
- Comparative Genomic
- Homology-based
	- machine learning: which I was familiar to

performance evaluation:
- accuracy
- precision
- recall
- F-measure

评判标准：
- of different TE

### CS existing library

Chinese Spring 转座子库文件格式：RepeatMasker -> CLARI-TE
- RepeatMasker:
	- The output of the program is 
		- a detailed annotation of the repeats that are present in the query sequence
		- a modified version of the query sequence in which all the annotated repeats have been masked (default: replaced by Ns).

提取转座子位点工具：SeqKit v2.6.1

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

analysis by perl code0

### EDTA

![[Pasted image 20240309220506.png]]

首先测试软件的时间较长，单是chr1A的就跑了一周：

- 只测chr1A/B/D
	- 也可以先做个比对，看有没有大的区别
- 将染色体切开，切成不同段的，从而实现多线程（丢弃一部分的断点数据）
	- 切成1Mbp的片段：速度提升很多
		- 最终结果是xxx，没有检测到真正有用的TE
	- 将gap也就是fa中显示N的片段作为切割处
		- cut_chr1A.sh

测试chr1A1M，结果：
- 线程：10
- 时间：8min
	- LTR: 1min
- 问题：
	- `Warning: LOC list chr1A1M.fa.mod.ltrTE.veryfalse is empty.`
		- 是在`Identify LTR retrotransposon candidates from scratch.`时产生的
	- `Species: others`：应当调节成小麦特定的检测方式
		- 物种特定的curated library
	- `-WARNING- Grid computing is not available because DRMAA not configured properly: Could not find drmaa library.  Please specify its full path using the environment variable DRMAA_LIBRARY_PATH`
		- 配置问题：
			- 是否安装DRMAA
			- 如何配置
	- `/data1/home/dazheng/miniconda3/envs/EDTA/lib/python3.6/site-packages/Bio/Seq.py:2338: BiopythonWarning: Partial codon, len(sequence) not a multiple of three. Explicitly trim the sequence or add trailing N before translation. This may become an error in future.  BiopythonWarning,`
		- 可能是Partial condon本身的问题，其中说的N，或许对检测结果有影响
	- `Unspecified/NA not found in the TE_SO database, it will not be used to rename sequences in the final annotation.`：无法找到的TE类型
		- 总共有50条
		- 是在导入`trep-db_complete_Rel-19.fasta`时发生的
			- trep-db有4126条：其中也找不到`Unspecified/NA'
		- TE_SO database：在TE_Sequence_Ontology.txt文件中，找到总共有记录的为87条

测试chr1AN：
- 切割后统计数据：
	- 片段数：20243
	- 平均长度：28932 << 1000000
		- 如果将片段平均长度改到大概1000000，有200个片段
		- 1M8min：$8\times200/60$，为27h，相比于原本7d也算是可以了
- 线程：25
- 时间：预估16h
	- LTR: 2h

测试chr1ANM：
- 切割后统计数据：
	- 片段数：242
	- 平均长度：2.45M
		- 1M8min：$8\times 2.5\times 242/60$，为80h

## library built (data 4)

# Population analysis

## reads mapping

二代测序：原理、reads长度、文件存储数据、二代分析测序流程
- 长度为几百bp：限制条件，也因此必须了解目标序列（转座子）的长度

将reads比对到基因组上的工具：bwa (bowtie2, or else)
- 目前已经有bam文件，无需继续计算

重测序数据 (resequencing data)：VMap 2 (>1000 accession)
1. Fastq
2. random selection: 10,000 reads
3. TE, blast

Vmap 2 数据包括：
- vcf文件：只包含了SNP位点/片段的reads比对到reference上
	- 也就是每个样本相对于reference的突变性
- bam文件：reads比对到reference上

三代测序长读段：直接检测TE
- fastq文件

## Population

后面再学习，先将现在的工作做好

load方面：主要参考郭亚龙，看插入
	- 使用数据：
		- 二代数据来扫：深度是否够，有一些难度
		- V2数据
		- 三代数据：建库，长reads能否建好
	- 目前无法找到位置，剪切型的转座子无法做，更多是复制型的变化
	- 转座子和RNA介导的甲基化过程，联系数据和机理