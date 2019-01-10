# Domain Labeling using rpstblastn
Using full CDD database:
 - rpstblastn with e-value cut-off of 1e-3
                   bitscore > 50 
 - output in JSON
 - split CDD database in :
    - Viral CDD
    - Cellular (eukaryotic) CDD
    - Prokaryotic CDD
    - mixed CDD

## Samples to test:
 - Negative:
    - No phage selection from data selection team
    - REFSEQ bacterial sequences (random 100 sequences, chopped in smaller pieces; cut-off: from 1kbp to 1Mbp)
    - REFSEQ cellular sequences (random 31 sequences belonging to fungi, invertebrate and protozoa)
    - optional: minimal Bacillus (deletion strains) WGS
 - Positive:
    - REFSEQ viral genomes
    - Selected SRA from data selection
    - crassphage DB (the 249 crAss-like phage contigs from Guerin et al., 2018)

## Metrics:
 - Evalue
 - Number of hits
 - Length of sequence and/or hit
 - Bitscore

## Output:
 - putative viral - pro - cellular
 - ambigious
 - unknowns

 - putative viral to phylogeny
 - drop PRO
 - drop cellular
 - ambigious / unkown to Genes / darkmatter?


##TODO:
 - run RPSTBLN
 - Chop positive control samples from REFSEQ
 - set up jupyter notebook for analysis + 
 - generate control samples + 
 - combine JSON formats 
