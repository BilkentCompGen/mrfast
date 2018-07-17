# mrfast

## micro-read Fast Alignment Search Tool

mrFAST is a read mapper that is designed to map short reads to reference genome with a special emphasis on the discovery of structural variation and segmental duplications. mrFAST maps short reads with respect to user defined error threshold, including indels up to 4+4 bp. This manual, describes how to choose the parameters and tune mrFAST with respect to the library settings. mrFAST is designed to find 'all'  mappings for a given set of reads, however it can return one "best" map location if the relevant parameter is invoked.

**NOTE:** mrFAST is developed for Illumina, thus requires all reads to be at the same length. For paired-end reads, lengths of mates may be different from each other, but each "side" should have a uniform length.
mrFAST : Micro-Read Fast Alignment Search Tool. Enhanced with FastHASH.

Usage: mrfast [options]

## General Options:  
&nbsp; **-v|--version**&nbsp; &nbsp; &nbsp; &nbsp; Current Version.  
&nbsp; **-h**&nbsp; &nbsp; &nbsp; &nbsp; Shows the help file.  


## Indexing Options:
&nbsp; **--index** [file]&nbsp; &nbsp; &nbsp; &nbsp; Generate an index from the specified fasta file.   
&nbsp; **--ws** [int]&nbsp; &nbsp; &nbsp; &nbsp; Set window size for indexing (default:12 max:14).  


## Searching Options:
&nbsp; **--search** [file]&nbsp; &nbsp; &nbsp; &nbsp; Search in the specified genome. Provide the path to the fasta file. Index file should be in the same directory.  
&nbsp; **--pe**&nbsp; &nbsp; &nbsp; &nbsp; Search will be done in Paired-End mode.  
&nbsp; **--seq** [file]&nbsp; &nbsp; &nbsp; &nbsp; Input sequences in fasta/fastq format [file]. If paired end reads are interleaved, use this option.  
&nbsp; **--seq1** [file]&nbsp; &nbsp; &nbsp; &nbsp; Input sequences in fasta/fastq format [file] (First file). Use this option to indicate the first file of paired end reads.   
&nbsp; **--seq2** [file]&nbsp; &nbsp; &nbsp; &nbsp; Input sequences in fasta/fastq format [file] (Second file). Use this option to indicate the second file of paired end reads.    
&nbsp; **-o** [file]&nbsp; &nbsp; &nbsp; &nbsp; Output of the mapped sequences. The default is "output".  
&nbsp; **-u** [file]&nbsp; &nbsp; &nbsp; &nbsp; Save unmapped sequences in fasta/fastq format.  
&nbsp; **--best**&nbsp; &nbsp; &nbsp; &nbsp; Only the best mapping from all the possible mapping is returned.  
&nbsp; **--seqcomp**&nbsp; &nbsp; &nbsp; &nbsp; Indicates that the input sequences are compressed (gz).  
&nbsp; **--outcomp**&nbsp; &nbsp; &nbsp; &nbsp; Indicates that output file should be compressed (gz).  
&nbsp; **-e** [int]&nbsp; &nbsp; &nbsp; &nbsp; Maximum allowed edit distance (default 4% of the read length).  
&nbsp; **--min** [int]&nbsp; &nbsp; &nbsp; &nbsp; Min distance allowed between a pair of end sequences.  
&nbsp; **--max** [int]&nbsp; &nbsp; &nbsp; &nbsp; Max distance allowed between a pair of end sequences.  
&nbsp; **--maxoea** [int]&nbsp; &nbsp; &nbsp; &nbsp; Max number of One End Anchored (OEA) returned for each read pair. We recommend 100 or above for NovelSeq use. Default = 100.  
&nbsp; **--maxdis** [int]&nbsp; &nbsp; &nbsp; &nbsp; Max number of discordant map locations returned for each read pair. We recommend 300 or above for VariationHunter use. Default = 300.  
&nbsp; **--crop** [int]&nbsp; &nbsp; &nbsp; &nbsp; Trim the reads to the given length.  
&nbsp; **--sample** [string]&nbsp; &nbsp; &nbsp; &nbsp; Sample name to be added to the SAM header (optional).  
&nbsp; **--rg** [string]&nbsp; &nbsp; &nbsp; &nbsp; Read group ID to be added to the SAM header (optional).  
&nbsp; **--lib** [string]&nbsp; &nbsp; &nbsp; &nbsp; Library name to be added to the SAM header (optional).  


