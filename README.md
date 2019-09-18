# ShannonMets
[Blood metabolome predicts gut microbiome α-diversity in humans](https://www.nature.com/articles/s41587-019-0233-9)
-------------------------------------------------------------------------------------------

DOI
https://doi.org/10.1038/s41587-019-0233-9

correspondence should be addressed to:  lhood@systemsbiology.org, sgibbons@systemsbiology.org, or nathan.price@systemsbiology.org 

The content is divided into two folders, one with the copies of notebooks used to generate main figures (as well as Supplementary Figure 2, which was originally a main figure) and one with code that can be run on the data to replicate our results. 

List of files in the FiguresNotebooks folder:
--------------------

**LASSO_RIDGE_METABOLOMICS_ANALYSIS.ipynb** - code used to generate analysis presented in figures 1 and 6 

**FIGURE_2.ipynb** -  code to generate Figure 2 

**HEATMAPS_FIGURE3_SUPP_FIGURE2_SUPP_FIGURE6.ipynb** -	Code to generate Figure 3, Supplementary figures 2 & 6 

**Regression_analysis_Figure_4and5.ipynb** - code used to generate analysis presented in figures 4 and 5

**RF_Classification_Mets_and_Clinical_Labs.ipynb**	- code used to generate analysis in figure 6 and supplementary figure 3

**Clinical_Labs_Proteomics_Regression_Analysis** - code used to generate analysis in figure 6C, performance of clinical labs and proteomics in predicting Shannon diversity in the discovery and validation cohorts

**Validation_compositional_microbiome-3 (1).csv**	microbiome -  composition median abundance data for validation cohort 

**corr_df (1).csv** -	correlation coefficients between metabolites and microbiome in discovery cohort 

**corr_df_validation-2 (1).csv** -	correlation coefficients between metabolites and microbiome in validation cohort 

**corr_pval (1).csv**	- p-values of correlation between metabolites and microbiome in discovery cohort

**corr_pval_validation-2 (1).csv** -	p-values of correlation between metabolites and microbiome in validation cohort 

**discovery_medians.csv** -	microbiome composition median abundance data for discovery cohort 

List of files in the ReplicationCode folder:
--------------------

**Metabolomics_Shannon.ipynb** - code used to predict Shannon diversity, as well as PD whole tree and Chao1, from plasma metabolomics. The code generates an R2 and extracts mean beta-coefficients from each of the ten cross-validations. RUN this code before proceeding to the Classification_Analysis or OLS_Regression, since these codes rely on .CSV files with the LASSO identified metabolites. 

Run order: 1
Needed input files: 'second_genome_2.csv', 'data_discovery.csv'
Generated output files: '_40_coefs.csv', 'top_11_mets.csv', 'coeff_validation.csv'

**CL_P_Shannon.ipynb** - code used to predict Shannon diversity from proteomics and Clinical labs across the discovery and validation cohorts. The code also calculates an R2 for different combinations of omics data.

Run order - independent
Needed input files: 'chemistries_git.csv', 'chemistries_val_git.csv', ...
'cleaned_proteomics.csv', 'proteomics_validation_impute.csv', 'data_discovery.csv'
Generated output files: None

**Classification_Analysis.ipynb** - code used to classify individuals in the bottom quartile of Shannon diversity using 11 plasma metabolites or a panel of clinical labs.

Run order: 2
Needed input files: 'chemistries_git.csv', 'second_genome_2.csv', 'data_discovery.csv', 'top_11_mets.csv'
Generated output files: None

**OLS_Regression.ipynb** - code used to generate Ordinary Least Square Regression models between each metabolite and Shannon. The code depends on a list of the 40 mets identified, which is generated using the "Metabolomics_Shannon" code. Same code can be used to generate OLS models for chemistries and proteomics.

Run order: 2
Needed input files: '_40_coefs.csv', 'data_discovery.csv'
Generated output files: 'supplementary_table_1.csv'

--------------------
Data files for code replication will be provided upon signature of a user agreement
--------------------



