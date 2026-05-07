# Targeted Marketing with Machine Learning

**Course**: MSIN0094 Marketing Analytics | UCL School of Management  
**Author**: Kuei-Chun Liu  
**Tools**: R · Quarto · dplyr · rpart · ranger

---

## Overview

This project builds a targeted marketing system for an Amazon Prime subscription campaign. Using RFM segmentation and supervised ML models, it identifies high-potential customers to maximise ROI while minimising wasted marketing spend.

## Contents

| File | Description |
|---|---|
| `assignment2_answer_sheet.qmd` | Full analysis in Quarto Markdown |
| `data_amazon.csv` | Amazon customer transaction data (5,000 customers) |

## Key Analyses

**1. Break-Even Response Rate**  
Computed the minimum response rate for the campaign to be profitable, used as a targeting threshold across all models.

**2. Blanket Marketing ROI**  
Baseline: sending offers to all 5,000 customers → ROI = −0.219 (loss)

**3. RFM Segmentation (K-Means Clustering)**  
Unsupervised customer segmentation using Recency, Frequency, and Monetary Value → ROI = 0.222

**4. Decision Tree**  
Supervised model trained on RFM features → ROI = 0.678 ✅ best interpretable model

**5. Random Forest (2,000 trees)**  
Ensemble model for improved stability → ROI = 0.494

## Key Finding

Supervised ML models significantly outperform blanket and unsupervised approaches. The decision tree achieved the highest ROI by directly learning from customer response labels.

## How to Run

1. Open `assignment2_answer_sheet.qmd` in RStudio
2. Ensure `data_amazon.csv` is in the same directory
3. Install required packages:
```r
pacman::p_load(dplyr, broom, rpart, rpart.plot, ranger)
```
4. Click **Render** to generate the HTML report
