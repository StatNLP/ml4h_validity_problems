This directory contains all files need to rerun the analyses related to the 
liver sofa example presented in the manuscript.

The most important files are the two R Markdown files (we recommed using RStudio
to open them):
[1] liver-analyze_trainData.Rmd
[2] liver-analyze_modelPredictions.Rmd


The directory data/ containes the raw data (train and test) needed to train the
DNN defined in /train-pytorch. In order to train this model from scratch you 
need to run train-pytorch/train_network.py. This scripts trains the DNN,
generates predictions (for test and train data) and also conducts the ablation 
study experiments. The results are stored in models/ and predictions/.
The script prepare_analysis_dataset.Rmd combines these results into the three 
analysis data sets train_set_with_sofa_predictions.rds, 
test_set_with_sofa_predictions.rds and ablation_set_with_sofa_predictions.rds 
which are used for analysis.

REMARK: If you knit the Rmd files you will obtain a pdf with the same name as
the script along with the figures in png,svg and pdf stored in figures/. The
computationally more expansiv sections are chached in *_cache/ directories.