# Logistic Regression Pipeline for Gene Counts

## Overview
This pipeline performs logistic regression on gene count data using various statistical techniques, including Lasso regression and Wilcoxon tests. The data has been transformed using CLR and processed via `phyloseq` to handle sparse counts.

## Input Data
1. `gene_count_matrix.txt`: Contains raw gene counts for all samples.
2. `sample_metadata.txt`: Contains sample information such as conditions (e.g., Insect groups).

## Workflow
The pipeline consists of the following major steps:
1. **Data Loading and Preprocessing**: Load the gene count matrix and metadata, filter the counts, and match samples.
2. **CLR Transformation**: Apply CLR (Centered Log-Ratio) transformation to normalize the gene counts.
3. **PCA and Ordination**: Perform PCA on the CLR-transformed data and visualize the results.
4. **Statistical Testing**: Use Wilcoxon tests to find significant differences between conditions.
5. **Differential Abundance Analysis**: Use ALDEx2 for differential abundance analysis.
6. **Logistic Regression**: Fit logistic regression models, including Lasso regularization, and validate model performance.

## How to Run
1. Clone the repository: 
   ```bash
   git clone https://github.com/Nikwando/pipeline_repository.git
