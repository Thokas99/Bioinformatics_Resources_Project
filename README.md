# Bioinformatic Resources Project

This project, undertaken as part of the Bioinformatic Resources course instructed by Alessandro Romanel during the academic year 2022-2023, focuses on the analysis of RNA-seq count data derived from various cancer datasets within the Cancer Genome Atlas (TCGA). The selected dataset specifically pertains to Lung Adenocarcinoma. A total of 50 tumor samples and 50 normal samples were randomly chosen from the original TCGA data.

## Report

**Authors:**
Thomas Sirchi

## Method

The method consist in:

1. **Load the RData file:**
   - Load the RData file to initiate the analysis.

2. **Extract protein-coding genes exclusively:**
   - Isolate protein-coding genes from the dataset.

3. **Conduct a differential expression analysis using the edgeR package:**
   - Identify up-regulated genes with a p-value cutoff of 0.01, a log fold change ratio >1.5 for up-regulation, < (-1.5) for down-regulation, and a log CPM >1.

4. **Perform gene set enrichment analysis using clusterProfiler:**
   - Utilize clusterProfiler for gene set enrichment analysis.

5. **Visualize an enriched pathway from the upregulated gene list using pathview:**
   - Use pathview to visualize an enriched pathway from the list of upregulated genes.

6. **Identify transcription factors (TFs) with enriched scores in the promoters of up-regulated genes:**
   - Identify TFs with enriched scores in the promoters of up-regulated genes.

7. **Select one top-enriched TF. Calculate empirical distributions of scores for all Position Weight Matrices (PWMs) found in MotifDB for the selected TF. Establish the distribution (log2) threshold cutoff at 99.75%:**
   - Choose a top-enriched TF and calculate empirical distributions for PWMs in MotifDB. Set the distribution threshold at 99.75%.

8. **Identify up-regulated genes with promoter regions having binding scores above the computed thresholds for any selected PWMs:**
   - Identify up-regulated genes with promoter regions having binding scores above the computed thresholds for selected PWMs.

9. **Discover Protein-Protein Interaction (PPI) networks among differentially expressed genes using the STRING database. Export the network in TSV format:**
   - Use the STRING database to find PPI networks among differentially expressed genes. Export the network in TSV format.

10. **Import the network using the igraph package. Identify and plot the largest connected component:**
    - Use the igraph package to import the network. Identify and plot the largest connected component.

*Adapted for a .md file for GitHub.*

