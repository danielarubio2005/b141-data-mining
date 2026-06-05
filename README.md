# B141 Data Mining — Individual Project
**Gisma University of Applied Sciences**  
Module: B141 Data Mining  
Assessment: Individual Project

---

## Project Overview
This project applies a full data mining pipeline to the 
UCI Online Retail II dataset, analysing transaction data 
from a UK-based online gift retailer (2010–2011) to extract 
actionable business insights.

## Research Questions
1. Which products are most frequently purchased together?
2. Are there anomalous transactions in the data?
3. Can customers be segmented by purchasing behaviour?

## Techniques Applied
| Technique | Method |
|---|---|
| Association Rule Mining | Apriori algorithm (built from scratch) |
| Outlier Detection | Z-score (scipy.stats) |
| Customer Segmentation | RFM Analysis + K-Means Clustering |

## Dataset
- **Source:** UCI Machine Learning Repository
- **Link:** https://archive.ics.uci.edu/dataset/502/online+retail+ii
- **Size:** ~541,000 transactions, 8 features
- **Period:** December 2010 – December 2011

## Repository Structure

- `b141_data_mining.ipynb` — Full annotated notebook
- `README.md` — This file

## Libraries Used
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn (KMeans, StandardScaler, silhouette_score)
- scipy (stats)

## How to Run
1. Open `b141_data_mining.ipynb` in Google Colab
2. Upload `online_retail_II.xlsx` to your Google Drive
3. Run all cells top to bottom

## Key Findings
- **35 association rules** identified, strongest lift = 22.2891
  (GREEN and PINK REGENCY TEACUP AND SAUCER)
- **99 outlier invoices** detected, representing 14.5% of 
  total revenue despite being only 0.53% of transactions
- **4 customer segments** identified (silhouette score = 0.616):
  Champions, Loyal Customers, Potential Loyalists, Lost Customers
