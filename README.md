# 🏠 House Prices Prediction - Kaggle Competition

My first Machine Learning project for the Kaggle competition. The goal is to predict house prices based on 79 features using Random Forest Regression.

## 📋 Project Overview

This project predicts residential home sale prices in Ames, Iowa using supervised learning. The model achieves a **Mean Absolute Error (MAE) of 17,296.77** on the validation set.

## 📁 Project Structure

```
house-price-prediction/
├── data/
│   ├── train.csv              # Training dataset (1460 houses)
│   └── test.csv               # Test dataset (1459 houses)
├── submissions/
│   └── submission.csv         # Kaggle submission file
├── housing_prices.ipynb       # Main notebook (exploration, training, evaluation)
├── predict_house.py           # Script to predict single house price
└── README.md                  # This file
```

## 🛠️ Technologies Used

- **Python 3.8+**
- **pandas** - Data manipulation
- **numpy** - Numerical operations
- **scikit-learn** - Machine learning algorithms

## 🚀 Installation

Install all required dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

Or use requirements file:
```bash
pip install -r requirements.txt
```

## 📊 Usage

### 1. Train and Evaluate the Model

Open the Jupyter Notebook to explore the complete workflow:

```bash
jupyter notebook housing_prices.ipynb
```

The notebook includes:
- ✅ Data exploration and visualization
- ✅ Feature engineering and preprocessing
- ✅ Model training (Random Forest Regressor)
- ✅ Cross-validation and evaluation
- ✅ Test predictions and submission generation

### 2. Predict a Single House Price

Run the prediction script:

```bash
python predict_house.py
```

Modify the `new_house` dictionary in the script with your house features (76 features required).

## 🔍 Model Details

### Preprocessing Pipeline

**Numerical Features (36):**
- Imputation: Median strategy
- Features: LotArea, GrLivArea, YearBuilt, TotalBsmtSF, etc.

**Categorical Features (40):**
- Imputation: Most frequent strategy
- Encoding: One-Hot Encoding
- Features: MSZoning, Neighborhood, HouseStyle, etc.

### Model Configuration

```python
RandomForestRegressor(
    n_estimators=130,
    max_depth=15,
    random_state=1
)
```

## 📈 Results

- **Validation MAE:** 17,296.77
- **Model:** Random Forest Regressor
- **Features Used:** 76 out of 79 available features
- **Preprocessing:** Automated pipeline with imputation and encoding

## 💡 Key Features

The model considers:
- **Location:** Zoning, neighborhood, lot configuration
- **Size:** Living area, lot area, number of rooms
- **Quality:** Overall quality and condition ratings
- **Age:** Year built and remodeled
- **Amenities:** Garage, basement, porch, pool features

## 📚 What I Learned

- Building end-to-end ML pipelines with scikit-learn
- Handling missing data with different imputation strategies
- Working with mixed data types (numerical and categorical)
- Feature engineering and selection
- Model evaluation and validation techniques
- Creating Kaggle competition submissions

## 🔮 Future Improvements

- [ ] Experiment with XGBoost and LightGBM models
- [ ] Advanced feature engineering (polynomial features, interactions)
- [ ] Hyperparameter tuning with GridSearchCV/RandomizedSearchCV
- [ ] Ensemble methods (stacking, blending)
- [ ] Handle outliers and perform better data cleaning
- [ ] Add feature importance analysis

## 🎯 Competition Details

**Competition:** House Prices - Advanced Regression Techniques  
**Dataset:** Ames Housing Dataset  
**Goal:** Predict the final sale price of homes  
**Evaluation Metric:** Root Mean Squared Error (RMSE)

## 👤 Author

**Achraf Bayane**  
First Machine Learning project - Kaggle House Prices Competition

---
📧 Feedback and suggestions are always welcome!
