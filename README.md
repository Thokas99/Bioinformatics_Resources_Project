# Bioinformatic Resources Project

This project, undertaken as part of the Bioinformatic Resources course instructed by Alessandro Romanel during the academic year 2022-2023, focuses on the analysis of RNA-seq count data derived from various cancer datasets within the Cancer Genome Atlas (TCGA). The selected dataset specifically pertains to Lung Adenocarcinoma. A total of 50 tumor samples and 50 normal samples were randomly chosen from the original TCGA data.

## Report

**Authors:**
Thomas Sirchi

## Method

The analysis begins by loading the RData file, serving as the foundation for subsequent steps. Following this, protein-coding genes are meticulously isolated from the dataset, setting the stage for a comprehensive analysis. Employing the edgeR package, a differential expression analysis ensues, delineating up-regulated genes based on stringent criteria encompassing a p-value cutoff of 0.01, a log fold change ratio exceeding 1.5 for up-regulation, and below (-1.5) for down-regulation, coupled with a log CPM surpassing 1. Gene set enrichment analysis is seamlessly executed using clusterProfiler, paving the way for a nuanced exploration of biological pathways. The visualization of enriched pathways from the upregulated gene list is achieved through the application of pathview. Subsequently, transcription factors (TFs) with enriched scores in the promoters of up-regulated genes are identified, with the top-enriched TF selected for further scrutiny. Calculating empirical distributions for all Position Weight Matrices (PWMs) in MotifDB, a distribution threshold is established at 99.75%. This threshold guides the identification of up-regulated genes with promoter regions exhibiting binding scores surpassing the computed thresholds for selected PWMs. The exploration expands to encompass Protein-Protein Interaction (PPI) networks among differentially expressed genes, employing the STRING database, with the resulting network exported in TSV format. Importantly, the igraph package is then employed to import the network, subsequently unveiling and plotting the largest connected component, providing a visual representation of intricate relationships within the PPI network.
