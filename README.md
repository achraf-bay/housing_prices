project:
  name: "Housing Prices Prediction"
  platform: "Kaggle – House Prices: Advanced Regression Techniques"
  description: >
    First Machine Learning project to predict house prices using
    supervised regression models. Supports both batch predictions
    and single house predictions.

features:
  batch_prediction:
    description: "Predict prices for multiple houses using test.csv and generate submission.csv for Kaggle."
    input: "data/test.csv"
    output: "submissions/submission.csv"
  single_house_prediction:
    description: >
      Predict price for a single house using predict_house.py.
      Define a dictionary of features matching the training data,
      convert it to a DataFrame, and use the trained pipeline to predict.
    script: "predict_house.py"

project_structure:
  data:
    - train.csv: "Training dataset with features + target SalePrice"
    - test.csv: "Test dataset with features only"
  submissions:
    - submission.csv: "Generated predictions for Kaggle submission"
  root_files:
    - README.md: "Project documentation"
    - housing_prices.ipynb: "Notebook with data analysis, preprocessing, and model training"
    - predict_house.py: "Python script for single-house predictions"

workflow:
  - "Load and explore data"
  - "Data cleaning and preprocessing"
  - "Feature engineering and encoding"
  - "Train regression model"
  - "Evaluate model"
  - "Predict prices for multiple houses (batch)"
  - "Predict price for a single house"
  - "Generate submission file for Kaggle"

tools_and_libraries:
  - Python
  - Pandas
  - NumPy
  - Scikit-learn
  - Jupyter Notebook

author:
  name: "Achraf Bayane"
  notes: "First Machine Learning project"

links:
  kaggle_competition: "https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques"

