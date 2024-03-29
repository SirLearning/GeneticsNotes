# build library

1. LTR retriever
	1. find LTR candidates
	2. LTR harvest: `-gt $genometools` `-size 1M`
	3. LTR finder: `-harvest_out` `-size 1M`
	4. LTR retriever: `-inharvest $genome.rawLTR.scn` `-trf_path $trf -blastplus $blastplus -repeatmasker $repeatmasker`
		1. full length LTR from `pass.list > LTR.intact.fa.ori`
		2. remove simple repeat: `mdust` `ori.dusted > ori.dusted.cln > LTR.intact.fa`
		3. generate annotated output: `intact.fa.ori, intact.fa > intact.fa.ori.rmlist + pass.list.gff3 > LTR.intact.gff`
2. TIR & Helitron: similiar, come to `EDTA.intact.fa, EDTA.intact.gff3`
3. filter LTR/TIR/Helitron candidates: combine dictionary
	1. purify: `raw.fa (like LTRlib.fa) > LTR.HQ, TIR.HQ, HEL.HQ`
		1. `TE_purifier`: purify a TE library based on another TE file containing the target contaminant, clearly divide LTR, TIR, and Helitron
		2. `cleanup_tandem`: clean up tandem repeat sequence and sequencing gap sequence in the fasta file
	2. clean LTR in TIR and HEL: `repeatmasker LTR.HQ + TIR.Helitron.fa.stg1.raw > err > TIR.Helitron.fa.stg1.raw.masked > TIR.Helitron.fa.stg1.raw.cln`
		1. `cleanup_tandem`: `TIR.Helitron.fa.stg1.raw.masked > TIR.Helitron.fa.stg1.raw.cln`
		2. cluster TIRs and Helitrons `cleanup_nested`: `TIR.Helitron.fa.stg1.raw.cln > $rename_TE LTR.TIR.Helitron.fa.stg1.raw.cln`
		3. remobe protein-coding sequence `cleanup_protein`: `LTR.TIR.Helitron.fa.stg1`
4. final TE/SINE/LINE scan: final dictionary
	1. input: `LTR.TIR.Helitron.fa.stg1, EDTA.intact.fa > EDTA.intact.fa.raw, EDTA.intact.gff3`
	2. identify remaining TEs in the genome:
		1. repeatmask
			1. `BuildDatabase: ncbi > $genome.masked`
			2. `RepeatModeler: ncbi, $genome.masked`
			3. `RM_*/consensi.fa > RM.consensi.fa`
		2. filter and reclassify RepeatModeler candidates with TEsorter
			1. TEsorter: `RM.consensi.fa`
				1. `rename_RM`: `RM.consensi.fa.rexdb.cls.lib > RepeatModeler.raw.fa`
			2. `repeatmasker`: `LTR.TIR.Helitron.fa.stg1, RepeatModeler.raw.fa > RepeatModeler.raw.fa.masked`
				1. `cleanup_tandem`: `RepeatModeler.raw.fa.masked > RepeatModeler.fa.stg1 + LTR.TIR.Helitron.fa.stg1 > LTR.TIR.Helitron.others.fa.stg2`
				2. `cleanup_protein`: `LTR.TIR.Helitron.others.fa.stg2 > LTR.TIR.Helitron.others.fa.stg2.clean > EDTA.raw.fa`
	3. final rounds of redundancy removal 
		1. `cleanup_nested`: `EDTA.raw.fa > EDTA.raw.fa.cln > EDTA.raw.fa.cln.cln`
		2. make final EDTA library `rename_TE`: `EDTA.raw.fa.cln.cln > EDTA.TElib.fa`
	4. remove known TEs in the EDTA library `RepeatMasker`: `EDTA.TElib.fa > EDTA.TElib.ori.fa + $HQlib > EDTA.TElib.fa, EDTA.TElib.novel.fa`
	5. reclassify intact TEs with the TE lib
		1. `RepeatMasker`: `EDTA.TElib.fa, EDTA.intact.fa > EDTA.intact.fa.out`
		2. reclassify `classify_by_lib_RM`: 
		3. `rename_by_list`: 
			1. `EDTA.intact.gff3, EDTA.intact.fa.rename.list > EDTA.intact.gff3.rename > EDTA.intact.gff3`
			2. `EDTA.intact.fa.rename > EDTA.intact.fa`