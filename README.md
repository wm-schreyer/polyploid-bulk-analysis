# polyploid-bulk-analysis

Pipeline for processing bulk transcript data from Illumina TruSeq. Software used: Trimmomatic, FastQC, HISAT2, StringTie, GffCompare

Steps:
1) Trimmomatic -> Trim raw sequence data to remove extras from Illumina i.e. adapters
2) FastQC -> Check quality of trimmed sequence data
3) HISAT2 -> Align output .fastq files to indexed A. thaliana genome, convert to .sam format
4) SAMtools -> Convert to .bam format, sort reads
4) StringTie -> Assemble sorted reads into transcripts for processing in R

Control Steps:
1) Trim, check sequence quality
2) Build ERCC control index, align to A. thaliana genome
3) Convert to .bam and sort
