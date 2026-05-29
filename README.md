Temporal Feature Engineering for Water Stress Classification in Olive Trees

This repository contains:
File                                                                   Purpose
notebooks/01_pipeline_complete.ipynb          Main pipeline: data loading, preprocessing, temporal feature engineering, benchmark,SHAP,LOVO notebooks/02_ablation_study.ipynb                           Ablation study (Static vs Temporal vs All), Figure 10, Wilcoxon tests
requirements.txt                                                               Python dependencies
figures/Output                                                              Output figures (PNG + PDF)
tables/                                                                     Output tables (CSV + LaTeX)

How to reproduce ?

1.The dataset is publicly available from Majikumna et al. (2025):
       URL: https://data.mendeley.com/datasets/22j26tpk63/1
       Download growth.xlsx and place it in the repository root.
2. Install dependencies
pip install -r requirements.txt
3. Run the notebooks in order
jupyter notebook notebooks/01_pipeline_complete.ipynb
jupyter notebook notebooks/02_ablation_study.ipynb

The first notebook produces the main benchmark results, SHAP analysis, and LOVO cross-validation. 
The second produces the ablation study and Figure 10.
Alternatively, the notebooks can be uploaded to Google Colab — no local installation required.
