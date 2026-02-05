# Data Science - Liver Cancer Analysis

### Step 1 : Clone this git repository
git clone https://git.imp.fu-berlin.de/data-science-group-5/data-science-liver-cancer-analysis.git
The input files from folder 'liver' are used each step.

### Step 2 : Do differential expression analysis for feature selection
Run the file "liver cancer mirna_mrna and methylation differential analysis.R" using R or R Studio. It will use the files from "liver" folder as input. Differentially expressed columns will be found for each type of data(mrna, mirna, methylation). Files named "Diff_mrnaupdated.csv", "Diff_methylupdated.csv" and "Diff_mirnaupdated.csv" will be generated and will be used in Step 4.

(Some of the output files generated for the Differential expression data produced could be commented out, to generate the output for those data please uncomment those lines).

### Step 3 : Do logistic regression analysis for feature selection + Machie Learling classification models for it
Run the python notebook "Logreg_part.ipynb" using Jupyter Notebook or Colab. It will use the files from "liver" folder as input. Number of features will be reduced using logistic regression. 2 binary classification models will be trained. "imp_features_svm_logreg.csv" and "imp_features_gb_logreg.csv" will be generated as output files, but only the first one will be used in Step 5 as results of the best model. The latter is provided if wanted for additional evaluation

### Step 4 : Machine Learling classification models for differntially expressed data
Run the python notebook "RDifferentialAnalysis_ML_Part.ipynb". It will use the files from "liver" folder + files generated in Step 2 as input. 2 binary classification models will be trained. "imp_features_gb_diff.csv" will be generated as an output file based on the best model. This file will be used in Step 5. 

### Step 5 : Survival Analysis
Run the python notebook "Survival Analysis.ipynb". It will use the files from "liver" folder + files generated in Step 3 and Step 4 as input. Survival analysis will be done for the important features found in Step 3 and Step 4
