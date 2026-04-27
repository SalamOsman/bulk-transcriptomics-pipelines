# Differential gene expression analysis of TCGA datasets.

A comprehensive analysis of the differential gene expression matrix from The Cancer Genome Atlas (TCGA) repository.

## Prerequisite for the analysis.

1. The installation of the R software and packages for counting raw reads
2. (Optional) Use the MS Windows generic text editor “Notepad,” and if you want a more efficient text editor, install either “TextPad” or “Notepad++”.

## Source for RNA-seq raw counts datasets and clinical files

* Broad GDAC firehose (https://gdac.broadinstitute.org/)
* Link of the TCGA mRNA preprocessed file used for this tutorial (http://gdac.broadinstitute.org/runs/stddata__2016_01_28/data/HNSC/20160128/gdac.broadinstitute.org_HNSC.mRNAseq_Preprocess.Level_3.2016012800.0.0.tar.gz)

In the case of an “error” when running libraries, ensure the installation of the corresponding library. (By typing the following command)

biocManager::install(“Name_of_the_library_to_be_installed”)

## Preparing the datasets

1. To create a metadata files, run "Preparing_meta_data_file.R" script.
2. Before starting the analysis, always create a separate directory so that it does not replace the files from the previous analysis, i.e., “C:/Users/User_name/Desktop/GitHub/HNSCC_DEGs/” on the Desktop.
3. In this tutorial, you will be using the mRNAseq_preprocess archived file of Head and Neck squamous cell carcinoma obtained from the Broad GDAC firehose. Decompress the downloaded file and import the file names as “HNSC.mRNAseq_raw_counts.txt” in R.
4. When assigning features to the raw counts, also retrieve the clinical archive file called “Clinical_Pick_Tier1”. After decompressing the file, restructure the file named “All_CDEs.txt” (Use the methodology described in the “Creating a meta-file from TCGA raw clinical file” session). For convenience, the “meta_data.txt” has been added to the current repository.

## Running the script

1. Change the directory path to your dataset location.
2. Customize the names of the input and output files as you like.
3. Run the script step by step.
4. Let’s see the score using statistical cutoffs for each gene in the resulting list, i.e., try adjusted p-value (padj) <0.05 and <0.02, and also absolute log2FoldChange >1 and >2.
5. Also, get a background knowledge for reading the plots and look at interesting observations.

If you need any help, please ask!

salam.abdus@mh-hannover.de

salam.nurzai@gmail.com
