# README
## About
This mini-project combines nutrition data from [McDonald's](https://www.kaggle.com/datasets/mcdonalds/nutrition-facts), [Burger King](https://company.bk.com/pdfs/nutrition.pdf) and [Subway](https://www.subway.com/en-US/MenuNutrition/Nutrition/NutritionGrid
) to see if there are any interesting insights to be gained from the aggregated data.

## Notebooks
1. [Data Preparation](data_prep.ipynb)

We merged the datasets together by removing unshared columns and matching the columns' data types. We also added useful categories (e.g. Meal Type - Breakfast/Main/Side) to help our analysis.

2. [Exploratory Data Analysis](eda.ipynb)

We visualized the data according to Restaurant and Meal Type. We also created an 'unhealthy index' as a marker of how unhealthy food items are according to recommended nutritional guidelines.

3. [K-Means Clustering](kmeans.ipynb)

We did K-Means Clustering on the numeric nutritional data. In order to reduce the dimensionality of the data, we performed Principal Component Analysis. We also did a Mains-specific clustering to look out for more distinct clusters. 

4. [Decision Tree Feature Selection](decision_tree.ipynb)

As there are many features in nutritional data, we used a Decision Tree to see which would be the most significant predictor for the unhealthy index. This most significant predictor could be used as a heuristic for avoiding unhealthier foods.

## Insights and Conclusion
Through our data visualization, we learnt that:
* **Breakfast** food items are generally the most unhealthy of all fast food items.
* Burger King has the highest proportion of healthy food items, followed by Subway

Through the multiple clusters from our data that we obtained through K-Means Clustering, we know that **relative to each other**:
* Burger King has the unhealthiest food items
* Subway has the largest selection of healthy foods
* McDonald’s items are actually on the healthier end relative to the other fast food chains

Through our decision tree, we know that:
* Avoiding saturated fats would be a useful heuristic in avoiding unhealthier food items when eating fast food.

## References
https://realpython.com/k-means-clustering-python/

https://www.analyticsvidhya.com/blog/2019/08/comprehensive-guide-k-means-clustering/
