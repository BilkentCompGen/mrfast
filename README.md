mrfast
======

micro-read Fast Alignment Search Tool

mrFAST is a read mapper that is designed to map short reads to reference genome with a special emphasis on the discovery of structural variation and segmental duplications. mrFAST maps short reads with respect to user defined error threshold, including indels up to 4+4 bp. This manual, describes how to choose the parameters and tune mrFAST with respect to the library settings. mrFAST is designed to find 'all'  mappings for a given set of reads, however it can return one "best" map location if the relevant parameter is invoked.

NOTE: mrFAST is developed for Illumina, thus requires all reads to be at the same length. For paired-end reads, lengths of mates may be different from each other, but each "side" should have a uniform length.

Wiki page: https://github.com/BilkentCompGen/mrfast/wiki
