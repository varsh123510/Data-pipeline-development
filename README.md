# Data-pipeline-development

**COMPANY NAME** CODTECH IT SOLUTIONS

**NAME** R.VARSHA

**INTERN ID** CT08JVZ 

**DOMAIN** : DATA SCIENCE

**BATCH DURATION** JANUARY 5th 2025 to FEBRUARY 5th 2025

**MENTOR NAME** NEELA SANTHOSH KUMAR

**DESCRIPTION OF THE TASK **
1. Dataset Creation

You create a small dataset with:

Two numeric columns: Age and Salary, which include some missing values.

One categorical column: City, representing city names.

One target column: Purchased, indicating whether something was purchased (Yes or No).

The dataset is stored in a pandas DataFrame for processing.

2. Splitting Features and Target

The dataset is split into:

Features (X): The independent variables (Age, Salary, and City) that will be used for predictions.

Target (y): The dependent variable (Purchased) you want to predict.

This helps separate what you’re working on (features) from what you’re trying to achieve (target).

3. Preprocessing Pipelines

This step handles missing values and transforms data to make it suitable for machine learning models.

Numeric Features

Missing values in numeric columns (Age and Salary) are replaced with the mean of each column.

After imputing missing values, the data is scaled (standardized) so that all numeric values have the same range, ensuring they contribute equally to the model.

Categorical Features

Missing values in the City column are filled with the most frequently occurring city (mode).

The City column is then one-hot encoded, converting city names into binary columns (e.g., City_New York, City_Chicago).

4. Combine Preprocessing Steps

You combine both transformations (numeric and categorical) into a single preprocessing pipeline using a ColumnTransformer. This ensures all preprocessing steps are applied in one go.

5. Transform the Data

The Pipeline is used to:

Apply preprocessing to X (features).

Transform numeric columns and expand categorical columns into one-hot encoded features.

This results in a numerical array where:

Numeric features (Age and Salary) are scaled.

Categorical features (City) are represented as multiple binary columns.

6. Convert Transformed Data to a DataFrame

After transformation:

Numeric features remain in their original format (scaled values).

Categorical features are replaced by their one-hot encoded binary columns.

The transformed data is converted back to a pandas DataFrame for readability, with new column names that include the numeric features and the one-hot encoded categorical columns.

7. Combine with Target Variable

Finally, the preprocessed features (X) are combined with the original target variable (y), resulting in a complete and ready-to-use dataset for machine learning tasks.
