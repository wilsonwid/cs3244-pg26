# Basic feature engineering

We conducted our feature engineering with the aim of producing as many useful features as possible to complement the raw data that has been provided. In order to do this, several things that we have done include:

* Dropping duplicate transactions
* Coercing low count categories to `OTHER` (as described in the exploratory data analysis portion)
* Converting datetime columns to simpler, numerical columns
* Extracting the middle floor number from `storey_range` as this indicates the 'average' value between the range of floors indicated.
* Remaining lease was imputed using a 99-year lease assumption for HDB flats, which was then transformed into `relative_tenure`.
* Using a per-square metre price instead of the resale price itself, due to a high correlation between them.

Moreover, we have included a basic Single Ordinary Least Squares (OLS) model to ensure that our data preprocessing is working as intended. This is different from our baseline model, which is a normal linear regression model implemented with [Scikit-learn](https://scikit-learn.org/stable/modules/classes.html) that we will detail more in the [Models](./models.md) section.

# Adding location data
In order to inject more features into the dataset, we decided to include some of the 