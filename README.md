# Ford Car Price Analysis & Prediction

A data analysis and machine learning project focused on analyzing Ford vehicle pricing patterns and building predictive models.

## Project Overview

This project performs exploratory data analysis (EDA) on Ford vehicle data and prepares features for price prediction modeling. The analysis covers various vehicle attributes including model type, transmission, fuel type, mileage, MPG, and engine size to understand their relationship with vehicle pricing.

## Dataset

**File:** `ford.csv`

**Features:**
- `model`: Ford vehicle model (Fiesta, Focus, Puma, Kuga, etc.)
- `year`: Year of manufacture
- `price`: Vehicle price (target variable)
- `transmission`: Automatic or Manual
- `mileage`: Vehicle mileage in miles
- `fuelType`: Petrol or Diesel
- `tax`: Annual tax amount
- `mpg`: Miles per gallon (fuel efficiency)
- `engineSize`: Engine displacement in liters

**Size:** Contains multiple Ford vehicle records with various specifications

## Project Structure

```
Ford/
├── README.md                          # Project documentation
├── Price_Prediction_Enhanced.ipynb    # Enhanced main analysis notebook (RECOMMENDED)
├── Price Prediction.ipynb             # Original analysis notebook
├── Untitled.ipynb                     # Initial EDA notebook
├── ANALYSIS_INSIGHTS.md               # Detailed insights and improvements
├── ford.csv                           # Dataset with Ford vehicle data
├── requirements.txt                   # Python dependencies
├── .gitignore                         # Git ignore patterns
└── data/                              # (Optional) Directory for processed data
```

## Analysis Workflow

### 1. **Data Loading & Overview**
   - Import necessary libraries (pandas, numpy, seaborn, matplotlib)
   - Load the CSV dataset
   - Display basic statistics (shape, describe, head)

### 2. **Exploratory Data Analysis (EDA)**
   - Correlation heatmap to identify relationships between features
   - Box plots for price distribution across:
     - Different vehicle models
     - Transmission types
     - Fuel types

### 3. **Data Preparation**
   - Feature engineering and selection
   - Dropping unnecessary columns
   - Preparing features (X) and target variable (Y) for modeling

### 4. **Feature Scaling & Preprocessing**
   - Standardizing features for machine learning algorithms
   - Handling categorical variables

## Key Insights

- **Correlation Analysis**: Identifies which features have the strongest relationship with vehicle price
- **Model Comparison**: Analyzes price variations across different Ford models
- **Transmission Impact**: Shows how transmission type affects pricing
- **Fuel Type Analysis**: Compares pricing between Petrol and Diesel vehicles

## How to Use

### Quick Start

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/Ford-Price-Prediction.git
   cd Ford
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Enhanced Notebook** (Recommended):
   ```bash
   jupyter notebook Price_Prediction_Enhanced.ipynb
   ```

4. **Execute all cells** to reproduce the analysis:
   - Use `Kernel → Restart & Run All` in Jupyter
   - Or run cells sequentially using Shift+Enter

### Notebook Options

- **Price_Prediction_Enhanced.ipynb** - Recommended version with comprehensive documentation, better structure, and fixed Model 2 implementation
- **Price Prediction.ipynb** - Original analysis notebook
- **Untitled.ipynb** - Initial EDA exploration

## Technologies Used

- **Python 3.8+**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **scikit-learn** - Machine learning models and metrics
- **seaborn** - Statistical data visualization
- **matplotlib** - Plotting library
- **Jupyter Notebook** - Interactive analysis environment

## Model Results

### Current Models

**Model 1: Linear Regression with All Features** (Including Transmission)
- R² Score: ~0.84
- Adjusted R²: ~0.84

**Model 2: Linear Regression without Transmission** (Recommended)
- R² Score: ~0.85  
- Adjusted R²: ~0.85
- Features: model, year, mileage, tax, mpg, fuelType, engineSize

### Key Findings

- Both models demonstrate **strong predictive capability** (84-85% accuracy)
- Transmission has minimal impact on price prediction
- All major features correlate with vehicle price
- Model 2 is slightly simpler with equivalent performance

## Output & Visualizations

The enhanced notebook generates:
- ✅ Statistical summaries and correlations
- ✅ Detailed heatmaps and distribution plots  
- ✅ Model performance metrics (R², MAE, RMSE)
- ✅ Side-by-side model comparison
- ✅ Feature-engineered datasets
- ✅ Prediction samples and error analysis

## Future Improvements

- [ ] Try ensemble methods (Random Forest, Gradient Boosting, XGBoost)
- [ ] Implement cross-validation for robustness
- [ ] Feature importance analysis
- [ ] Hyperparameter tuning and optimization
- [ ] Build REST API for price predictions
- [ ] Deploy model to production

## Notes

- **Data Assumptions**: Features are properly scaled (StandardScaler)
- **Categorical Encoding**: Uses one-hot encoding for categorical variables
- **Train/Test Split**: 80/20 split with random_state=42 for reproducibility
- **Missing Values**: Dataset checked and no missing values found

## Author

Created for Ford vehicle price analysis and prediction

## License

Open for educational and analysis purposes

---

**Last Updated:** July 3, 2026

**Status:** ✅ Complete - EDA, Feature Engineering, Model Development, and Evaluation phases finished

**Version:** 1.0 (Enhanced)

**GitHub Repository:** [Ford-Price-Prediction](https://github.com/yourusername/Ford-Price-Prediction)

**Author:** Harsh

**License:** Open for educational and analysis purposes
