# **Comprehensive Analysis of Defense Mechanisms in *Acinetobacter* spp. Using Padloc and R**

## **Project Overview**
This repository contains the code and data for the analysis of defense mechanisms in *Acinetobacter* spp., focusing on gene expression profiling under stress conditions. The study uses the **Padloc** tool for defense gene identification and **R** for data analysis and visualization.

## **Dataset Information**
- **Dataset**: GSE120392 (Characterization functional of AcoN-like negative regulator protein from Acetoin cluster in *Acinetobacter* spp.)
- **Source**: Gene Expression Omnibus (GEO) - [GSE120392](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE120392)
- **Description**: The dataset includes expression profiles from *Acinetobacter* strains under various environmental stress conditions, such as oxidative stress (ROS response) and exposure to heavy metals. The study aims to characterize the role of defense mechanisms such as CRISPR-Cas, restriction-modification systems (R-M), and toxin-antitoxin systems (TA).

## **Tools and Technologies**
- **Padloc**: Used for defense gene identification, scanning the bacterial genome for known and novel defense systems (e.g., CRISPR-Cas, R-M, TA systems).
- **R**: Used for the statistical analysis and visualization of genomic data, including heatmaps, gene presence/absence matrices, and phylogenetic trees.

## **Repository Structure**
```bash
├── data/                     # Folder containing raw and processed datasets
│   ├── GSE120392_family.soft.gz  # Metadata file
│   ├── GSE120392_series_matrix.txt.gz  # Expression matrix
│   └── GSE120392_RAW.tar      # Raw data files (optional)
├── scripts/                  # R scripts for analysis and visualization
│   ├── padloc_analysis.R      # Script to run Padloc on genome data
│   ├── data_visualization.R   # R script to generate visualizations (heatmaps, phylogenetic trees)
├── results/                  # Folder for analysis outputs and figures
│   ├── defense_genes.csv      # Padloc output (detected defense genes)
│   ├── heatmap_defense_genes.png   # Heatmap of defense gene distribution
├── README.md                 # Project documentation
└── LICENSE                   # License file (if applicable)
```

## **How to Use**
1. **Download the Dataset**:
   - The dataset can be accessed and downloaded from the GEO database under accession number [GSE120392](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE120392).

2. **Install Required Tools**:
   - Install Padloc for defense gene identification:
     ```bash
     git clone https://github.com/padlocbio/padloc
     cd padloc
     make install
     ```
   - Install R and the necessary libraries for data analysis:
     ```r
     install.packages(c("GEOquery", "pheatmap", "ggplot2", "phytools"))
     ```

3. **Run Analysis**:
   - Run **Padloc** on the genome data to identify defense genes:
     ```bash
     ./padloc genome.fasta -o defense_genes.csv
     ```
   - Use the provided R scripts in the `scripts/` folder to perform the analysis and generate visualizations:
     ```r
     source("scripts/padloc_analysis.R")
     source("scripts/data_visualization.R")
     ```

## **Analysis Goals**
- **Identify defense genes** (e.g., CRISPR-Cas, R-M, TA systems) in *Acinetobacter* spp.
- **Visualize the distribution of defense genes** across samples using heatmaps.
- **Explore the relationship between defense genes and stress response** under different environmental conditions.

## **Results**
The output of the analysis includes:
- **Defense gene profiles** across different *Acinetobacter* strains.
- **Heatmaps** visualizing the presence and absence of defense genes across samples.
- **Phylogenetic trees** showing the evolutionary relationship of defense gene systems.

## **References**
- GEO Dataset: [GSE120392](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE120392)
- Sorek Lab Publications: [Sorek Lab, Weizmann Institute](https://www.weizmann.ac.il/molgen/sorek/publications)

## **License**
This project is licensed under the MIT License. See the LICENSE file for more details.
