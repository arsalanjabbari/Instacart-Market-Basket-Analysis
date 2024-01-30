#  Instacart Market Basket Analysis

I have been provided with a set of files that describe customers' orders over time. The dataset comprises a sample of over 3 million grocery orders from more than 200,000 users. For each user, it includes between 4 and 100 of their orders, along with the sequence of products purchased in each order.

The [dataset](https://www.kaggle.com/competitions/instacart-market-basket-analysis/data) is sourced from [Kaggle](https://www.kaggle.com/), and the project unfolds in two distinct phases:

## Data Preprocessing and Analysis:
In this initial phase, we meticulously preprocess and analyze the dataset, laying the foundation for subsequent stages.

After cleaning the data and eliminating any NaN values, our analysis encompasses the following key aspects:

- **Grouping by Products in Each Order:** Organizing products based on individual orders, creating baskets for each order.

- **Product Order Frequency:** Determining how frequently each product was ordered to identify popular items.

- **Orders per Department Visualization:** Calculating and visually representing the number of orders per department.

- **Customer Shopping Patterns:** Investigating customer behavior by analyzing:
    - **Weekday Order Frequency:** Examining the frequency of orders on weekdays.

    - **Hourly Order Frequency:** Analyzing the frequency of orders during different hours of the day, visualizing the patterns.

    - **Re-order Ratio Heatmap:** Plotting a heatmap depicting the re-order ratio based on the day of the week and hour of the day.

- **Re-ordered Product Ratio Visualization:** Determining and visualizing the ratio between reordered and non-reordered products to gain insights into customer preferences.

- **Most Popular Aisles:** Identifying and highlighting the aisles that attract the highest customer engagement to unveil popular shopping sections.

- **Top 10 Ordered Products:** Showcasing the top 10 products that consistently rank as customer favorites, providing insights into preferred items.

- **Days Since Prior Order Distribution:** Analyzing and visualizing the distribution of days elapsed since the last order, offering a comprehensive view of customer ordering patterns over time.

## Association Rule Mining with Apriori:
The second phase revolves around the implementation of Apriori for Association Rule Mining. This step involves extracting meaningful patterns and associations from the preprocessed data, contributing to the overall project insights.

### Overview
The Apriori algorithm is a classic algorithm in data mining and association rule learning. It is used for discovering interesting relationships or associations among a set of items in large datasets. The primary motivation behind the Apriori algorithm is to identify frequent itemsets, which are subsets of items that appear together frequently in the dataset. These frequent itemsets are then used to generate association rules that describe relationships between different items.

### Why Apriori Algorithm?
The Apriori algorithm is particularly useful in market basket analysis, where it helps uncover patterns in customer purchase behavior. By identifying frequent itemsets and association rules, businesses can gain insights into which products are often bought together. This information is valuable for strategies such as product placement, cross-selling, and targeted marketing.

### Code Explanation

#### Parameters
- `baskets_values`: List of transactions or baskets.
- `min_support`: Minimum support threshold for identifying frequent itemsets.
- `min_confidence`: Minimum confidence threshold for generating association rules.

#### Functions
1. `generate_candidate_itemsets(data, k)`: Generates candidate itemsets of size k from the input data.
2. `calculate_support(data, candidates)`: Calculates the support of each candidate itemset in the dataset.
3. `prune_non_frequent_itemsets(support, min_support)`: Prunes non-frequent itemsets based on the minimum support threshold.
4. `apriori_algorithm(data, min_support)`: Applies the Apriori algorithm to find frequent itemsets.
5. `generate_association_rules(frequent_itemsets, data, min_confidence)`: Generates association rules from frequent itemsets.

#### Running the Algorithm
The code initializes parameters such as `baskets_values`, `min_support`, and `min_confidence`. It then applies the Apriori algorithm to find frequent itemsets and subsequently generates association rules. The results are printed, including frequent itemsets with their support and association rules with confidence and lift.






## Prerequisites:
Before running the code, ensure that you have the following prerequisites:

- [Python](https://www.python.org/)
- [Jupyter Notebook](https://jupyter.org/)
- itertools library
- [pandas](https://pandas.pydata.org/) library
```bash
pip install pandas
```
- [plotly](https://plotly.com/) library
```bash
pip install plotly
```
