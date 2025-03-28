# Mid-Cayman-Rise-RNA-SIP
Bioinformatics analysis of data generated from sequencing 1) metagenomes of unmanipulated diffuse deep-sea hydrothermal vent fluid 2) metatranscriptomes of these same fluids and 3) metatranscriptomes from RNA-SIP (with 13C-bicarb) incubations from these same fluids. This analysis will provide insight into the active microbial autotrophs in these subseafloor crustal fluids. 

QC, trimming, assembly, and binning of the unmanipulated fluid metagenomes were done with the EukHeist pipeline (Alexander et al., 2022), so that all samples were assembled (megahit) and binned (METABAT). Outputs from EukHeist included over 800 metagenomic bins, where only 18 were putatively identified as eukaryotic, leaving the majority of the bins to be analyzed for bacteria and archaea.

QC and trimming of the unmanipulated fluid metatranscriptomes were done using the eukrhythmic pipeline (A. I. Krinos et al., 2023). 

## Scripts/notes:
### For handling the metagenomic contigs: 
1) Annotation of the 800 MAGs using Prokka v1.14.6-> prokka_bins_MCR
2) Annotation of the metagenomic contigs using Prokka v1.14.6 -> prokka_contigs_MCR
3) Classifying taxonomy of metagenomes using GTDB_tk v2.4.0 with prodigal v2.6.3 -> GTDBtk_contigs_MCR
4) 
   
### For handling the RNA-SIP metaT's:
1) Tar unzip the sequencing files -> tar_unzip_MCR
2) Trim adapter sequences using fastp v0.24.0 -> fastp_metaTs_MCR
3) Fastp v0.24.0 results -> fastp_metaTs_MCR_results
4) Download SILVA rRNA DBs v138.2 -> SILVA_DB_Download
5) Remove eukaryotes from the SSU and LSU database and concatenate with the RFAM 5S database to make a prokaryotic reference rRNA file -> make_rRNA_ref_db
6) Separate non-coding RNA from coding RNA in trimmed, QC'd RNA-SIP metaT's using SortMeRNAv4.3.6 -> sortmerna_MCR
