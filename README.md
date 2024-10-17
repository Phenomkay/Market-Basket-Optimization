# Project Title: Market Basket Analysis Using Association Rule Mining

## Project Overview
This project applies market basket analysis through association rule mining to identify relationships between items commonly purchased together. Using the Apriori algorithm, we analyze transactional data to extract actionable insights, potentially useful for product placement and promotional strategies.

## Problem Statement
Retailers often lack insights into which products are frequently bought together, limiting opportunities for targeted promotions and inventory optimization. Identifying associations in customer purchases can help address this challenge and improve marketing and operational efficiency.

## Project Objective
The objective of this project is to utilize the Apriori algorithm to identify and analyze frequent item combinations in a transactional dataset. The goal is to generate insights based on key metrics like support, confidence, and lift, offering actionable recommendations for retail strategy.

---

## Steps in the Analysis

### 1. Import Libraries
The necessary libraries were imported to handle data processing, visualizations, and warnings. This step ensures a smooth setup for the analysis process.

### 2. Load the Dataset
The dataset, which contains transactional data of purchases, was loaded for analysis. Each transaction represents a customer's basket and the items it contains.

### 3. Data Preprocessing
The raw dataset was converted into a transactional format that could be used by the Apriori algorithm. Each transaction was represented as a list of items, making it ready for mining frequent itemsets.

### 4. Applying the Apriori Algorithm
Using the Apriori algorithm, association rules were generated based on specific parameters, including minimum support, confidence, and lift thresholds. This step identifies meaningful item combinations and relationships among items based on these metrics.

### 5. Extracting and Storing Results
The algorithm results were then parsed and organized into lists for the following metrics:
   - **Left-hand side (LHS)**: The item(s) in the "if" part of the rule.
   - **Right-hand side (RHS)**: The item(s) in the "then" part of the rule.
   - **Support**: The frequency with which the itemset appears in the dataset.
   - **Confidence**: The likelihood of buying the RHS item(s) given the LHS item(s).
   - **Lift**: Indicates the strength of the association by showing how much more likely items are bought together than independently.

   These lists were then combined into a DataFrame, allowing for easier sorting and filtering of the rules based on various metrics.

### 6. Visualization and Insights
Heatmaps were created for support, confidence, and lift to visually analyze the strength and frequency of associations between items:


- **Support Heatmap**: Showcases the frequency of item combinations, with higher values indicating frequently purchased pairs.

![Support Heatmap](https://github.com/Phenomkay/Market-Basket-Optimization/blob/28a836c4b2c6eafee289ce97342bb65e12d1c40b/support%20heatmap.png)

**Key observations:**

 - The highest support value (0.0160) is for "herb & pepper" and "ground beef."

 - Notable support values include "light cream" and "chicken" (0.0045), and "whole wheat pasta" and "olive oil" (0.0080).
   


- **Confidence Heatmap**: Illustrates the probability of buying the RHS item(s) when the LHS item(s) are bought, with higher values suggesting stronger predictive relationships.
  
![Confidence Heatmap](https://github.com/Phenomkay/Market-Basket-Optimization/blob/28a836c4b2c6eafee289ce97342bb65e12d1c40b/confidence%20heatmap.png)

**Key observations:**

 - Herb & Pepper and Ground Beef (0.3235) - high confidence

 - Pasta and Escalope (0.3729) - notable pairing

 - Tomato Sauce and Escalope (0.3774) - strong relationship



- **Lift Heatmap**: Highlights the strength of associations by showing how much more likely items are bought together than expected by chance, with high lift values pinpointing valuable itemsets.

![Lift Heatmap](https://github.com/Phenomkay/Market-Basket-Optimization/blob/28a836c4b2c6eafee289ce97342bb65e12d1c40b/lift%20heatmap.png)

**Some high lift values include:**

 - Fromage blanc and honey: 5.1643

 - Herb & pepper and ground beef: 3.2920

 - Light cream and escalope: 4.8440

 - Pasta and escalope: 4.7008

 - Whole wheat pasta and olive oil: 4.1224

### Key insights:

By analyzing the heatmaps:
- **High-confidence pairings**: Herb & Pepper and Ground Beef (0.3235) and Pasta and Escalope (0.3729) stand out.

 - **Strong relationships**: Fromage blanc and Honey, Light Cream and Escalope, Whole Wheat Pasta and Olive Oil all have high lift values.

### Recommendations:

**Marketing**: Target promotions around these pairs, offering discounts or special deals to boost sales.

**Inventory Management**: Ensure these items are always stocked together to meet demand and improve customer satisfaction.

**In a nutshell**: smart pairings lead to happy customers and optimized sales strategies! 😊

## Conclusion
This analysis successfully uncovers meaningful associations within the dataset, offering actionable insights for retail strategies like targeted promotions and optimized product placements. The metrics and visualizations provide a clear understanding of key item relationships, helping to enhance sales and customer satisfaction.
