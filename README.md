# Mid-Cayman-Rise-RNA-SIP
bioinformatics analysis of data generated from sequencing 1) metagenomes of unmanipulated diffuse deep-sea hydrothermal vent fluid 2) metatranscriptomes of these same fluids and 3) metatranscriptomes from RNA-SIP (with 13C-bicarb) incubations from these same fluids. This analysis will provide insight into the active microbial autotrophs in these subseafloor crustal fluids. 

QC, trimming, assembly, and binning of the unmanipulated fluid metagenomes were done with the EukHeist pipeline (Alexander et al., 2022), so that all samples were assembled (megahit) and binned (METABAT). Outputs from EukHeist included over 800 metagenomic bins, where only 18 were putatively identified as eukaryotic, leaving the majority of the bins to be analyzed for bacteria and archaea.

QC and trimming of the unmanipulated fluid metatranscriptomes were done using the eukrhythmic pipeline (A. I. Krinos et al., 2023). 

Contents:
1) Script for (and notes on) the annotation of the 800 MAGs  - prokka_bins_MCR
2) Script for (and notes on) the annotation of the metagenomic contigs - prokka_contigs_MCR
