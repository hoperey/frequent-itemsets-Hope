# Frequent Itemsets Project

## Made by: **Hope Kimandi** – hopekendi86@gmail.com 


## Project Overview
This project simulates supermarket transactions and applies frequent pattern mining using the Apriori algorithm.  
It demonstrates the generation of frequent, closed, and maximal itemsets from supermarket data.


## Objectives and How They Were Achieved

1. **Simulate at least 3000 supermarket transactions with 2–7 items from a pool of 30+ items**
   - A simulation of 4000 supermarket transactions with 2-7 items from a pool of 33 items was created on Python. 
   - Achieved using Python's `random.sample()` and a predefined `item_pool` of 30 items.  
   - Transactions were stored in a list and exported to `supermarket_transactions.csv`.  
   - Code in `frequent_itemsets_analysis.ipynb` under the **Data Generation** cell.

3. **Convert transactions into one-hot encoded format**  
   - Used `pandas.DataFrame` to create a zero-filled table with transactions as rows and items as columns.  
   - Looped through each transaction and set `1` where items were present.  
   - Exported as `supermarket_onehot.csv`.  
   - Code is under the **Preprocessing (one-hot)** cell.

4. **Generate frequent itemsets using Apriori with minimum support 0.05**  
   - Implemented a custom Apriori algorithm in Python.  
   - The algorithm generates frequent 1-itemsets, then iteratively produces larger itemsets.  
   - Support counts and support values are calculated and stored.  
   - Output exported as `frequent_itemsets.csv`.

5. **Identify closed frequent itemsets**  
   - Closed itemsets are those that do not have any proper superset with the same support.  
   - Iterated through all frequent itemsets to filter only closed ones.  
   - Exported as `closed_itemsets.csv`.  
   - Code is under the **Closed Itemsets** section.

6. **Identify maximal frequent itemsets**  
   - Maximal itemsets are those that do not have any frequent proper superset.  
   - Iterated through all frequent itemsets and filtered maximal ones.  
   - Exported as `maximal_itemsets.csv`.  
   - Code is under the **Maximal Itemsets** section.


## Files Included

| File | Description |
|------|-------------|
| `supermarket_transactions.csv` | Raw simulated transactions |
| `supermarket_onehot.csv` | One-hot encoded transaction table |
| `frequent_itemsets.csv` | Output of Apriori (all frequent itemsets) |
| `closed_itemsets.csv` | Filtered closed frequent itemsets |
| `maximal_itemsets.csv` | Filtered maximal frequent itemsets |
| `frequent_itemsets_analysis.ipynb` | Fully commented Jupyter notebook with all code |


## Notes

- All code is fully commented line-by-line using the format: `# Student: Hope`.  
- The dataset was entirely generated in Python (no Excel used).  
- This README explicitly explains how each objective was achieved in code.  
