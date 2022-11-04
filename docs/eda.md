Exploratory data analysis is a crucial part in any machine learning project, as it allows one to discover more insights about the data before fully committing to a certain approach in going through the project. 

In achieving this goal, we:

1. Collated all our data into a single, unified dataset where all our analysis will be conducted in
2. Plotted bar charts of the various categories for `flat_model`, `town`, and `flat_type` to detect categories that have very small counts. This is to group these into an `other` group that represents the minority categories for each feature.
3. Used `pandas_profiling` to allow for automated EDA report generation. The report is available [here](df_combined_report.html).

From this initial phase of our project, we are able
