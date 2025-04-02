# financial-association-rules




## Overview

This project analyzes financial transaction data to discover interesting associations between different financial products/services that customers use together, using association rule mining (Apriori algorithm).

## Key Features

- Exploratory Data Analysis of financial product usage
- Association rule mining with Apriori algorithm
- Visualization of product co-occurrence patterns
- Business insights generation for financial services

#About the Apriori Algorithm
The Apriori algorithm is a classic association rule mining technique used to identify frequent itemsets and generate association rules in transactional databases. It operates on the principle that "if an itemset is frequent, then all its subsets must also be frequent."

#Key Concepts:
Support:

Measures how frequently an itemset appears in the dataset

Support(X) = (Transactions containing X) / (Total transactions)

Confidence:

Measures how often items in Y appear in transactions containing X

Confidence(X → Y) = Support(X ∪ Y) / Support(X)

Lift:

Measures how much more likely Y is purchased when X is purchased

Lift(X → Y) = Confidence(X → Y) / Support(Y)

#How It Works:
Frequent Itemset Generation:

Identifies all itemsets that meet a minimum support threshold

Uses a "bottom-up" approach where frequent subsets are extended

#Rule Generation:

Creates association rules from frequent itemsets

Filters rules based on minimum confidence thresholds

#Why We Used It:
Well-suited for market basket analysis (like our financial products case)

Efficiently handles large datasets by pruning unlikely candidates

Provides interpretable metrics (support, confidence, lift) for business decisions

Works well with binary/transactional data like our financial product usage

#Implementation Notes:
In this project, we used:

Minimum support of 0.2 (20% of transactions)

Minimum confidence of 0.7 (70% probability)

The mlxtend library's implementation of Apriori
