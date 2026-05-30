Temporal Feature Engineering for Water Stress Classification in Olive Trees

This repository contains these files:
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
jupyter notebook notebooks/Pipeline_Complet_Etape1_et_2.ipynb
jupyter notebook notebooks/Etape_3_Ablation_Et_Figures_Finales.ipynb
jupyter notebook notebooks/Etape_4_Bootstrap_CI.ipynb
Or Directly Etape_1_FINAL_Features_Temporelles.ipynb:
The first notebook produces the main benchmark results, SHAP analysis, and LOVO cross-validation. 
The second produces the ablation study and Figure 10.
Alternatively, the notebooks can be uploaded to Google Colab — no local installation required.

Key results:
Configuration              N features        N classes           Macro F1 
A — Static only                 8               4              0.402 ± 0.021
B — Enriched                    24              4              0.789 ± 0.046 
C — Enriched                    24              3              0.844 ± 0.043

Ablation study (Wilcoxon signed-rank, paired across 16 cumulative-week cutoffs):
 -Temporal-only vs Static-only: ΔF1 = +0.332, p < 0.001
 -All vs Temporal-only: ΔF1 = −0.017, p = 1.0 (n.s.)

