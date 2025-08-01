# Customer Spending Prediction with Linear Regression

## Project Overview

This notebook analyzes customer data from a fictional e-commerce company to predict annual spending patterns. The project uses exploratory data analysis (EDA) and a linear regression model to:

- Identify which customer features correlate most strongly with spending
- Help the company decide whether to invest more in website or mobile app improvements

## Table of Contents

1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Dataset](#dataset)
4. [Key Steps](#key-steps)

   * [Data Loading & Initial Exploration](#data-loading--initial-exploration)
   * [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
   * [Data Preparation](#data-preparation)
   * [Model Building](#model-building)
   * [Evaluation](#evaluation)
   * [Insights & Recommendations](#insights--recommendations)
5. [Business Applications](#business-applications)
6. [Prerequisites](#prerequisites)
7. [Installation](#installation)
8. [Key Findings](#key-findings)
9. [Model Summary](#model-summary)

   * [Coefficient Interpretation](#coefficient-interpretation)
   * [Model Evaluation](#model-evaluation)
10. [Contributing](#-contributing)
11. [Contact](#-contact)

## Technologies Used

- **Python** (Primary programming language)
- **Pandas** (Data manipulation and analysis)
- **NumPy** (Numerical computing)
- **Matplotlib/Seaborn** (Data visualization)
- **Scikit-learn** (Machine learning implementation)
  - `train_test_split` (Data splitting)
  - `LinearRegression` (Model implementation)
  - Evaluation metrics (`mean_absolute_error`, `mean_squared_error`, `r2_score`)

## Dataset

The dataset (`Ecommerce Customers.csv`) contains information about 500 customers with the following features:

- `Email`
- `Address`
- `Avatar`
- `Avg. Session Length`
- `Time on App`
- `Time on Website`
- `Length of Membership`
- `Yearly Amount Spent` (Target variable)

## Key Steps

1. **Data Loading & Initial Exploration**
   - Imported and examined the dataset structure
   - Checked for missing values and data types

2. **Exploratory Data Analysis (EDA)**
   - Visualized relationships between features
   - Identified correlations with spending

3. **Data Preparation**
   - Selected relevant features
   - Split data into training and test sets

4. **Model Building**
   - Implemented Linear Regression
   - Trained the model on customer data

5. **Evaluation**
   - Assessed model performance using metrics:
     - Mean Absolute Error (MAE)
     - Mean Squared Error (MSE)
     - R-squared (R²) score

6. **Insights & Recommendations**
   - Determined which factors most influence spending
   - Provided actionable business recommendations

##  Business Applications

This analysis helps e-commerce businesses:
- Understand customer behavior patterns
- Optimize resource allocation between website and app development
- Develop targeted marketing strategies
- Improve customer retention and revenue


### Prerequisites
- Python 3.x
- Jupyter Notebook
- Libraries listed in the first code cell

### Installation
1. Clone the repository
2. Install required packages: `pip install pandas numpy matplotlib seaborn scikit-learn`
3. Open the notebook in Jupyter: `jupyter notebook Consumer_Spend_Prediction_ML_Model.ipynb`

## Key Findings

Right now, the mobile app is linked to more customer spending than the website. But before deciding what to focus on, it’s a good idea to dig a bit deeper.

You should look at how Length of Membership relates to both App and Website usage. For example:

1. Do older customers prefer one platform over the other?

2. Are new users more active on the app?

Answering these kinds of questions can help you decide whether to:

a. Improve the website to make it more engaging, or

b. Keep investing in the app, since it's already performing well.

The best decision depends on what your users are doing and what the company wants to achieve.

## Model Summary

### Coefficient Interpretation

| Feature                  | Coefficient | Interpretation                                                               |
| ------------------------ | ----------- | ---------------------------------------------------------------------------- |
| **Avg. Session Length**  | +25.98      | Spending increases by **\$25.98** for every unit increase in session length. |
| **Time on App**          | +38.59      | Spending increases by **\$38.59** for every unit increase in app time.       |
| **Time on Website**      | +0.19       | Spending increases slightly by **\$0.19** per unit increase in website time. |
| **Length of Membership** | +61.27      | Strongest predictor: adds **\$61.27** per extra year of membership.          |

These coefficients were obtained using a multiple linear regression model. All variables were assumed to be linearly independent with minimal multicollinearity.

### Model Evaluation

| Metric                   | Value  |
| ------------------------ | ------ |
| Mean Absolute Error      | 12.02  |
| Mean Squared Error       | 240.10 |
| Root Mean Squared Error  | 15.49  |
| R² Score (Explained Var) | 0.98   |

R² score of **0.98** indicates the model explains **98%** of the variability in customer spending — a strong fit.

## Performance Chart (Actual vs Predicted Spending)

<img width="575" height="457" alt="prediction" src="https://github.com/user-attachments/assets/1f25aab3-9a3b-4981-9472-a229b9dc388a" />


This chart shows how well my model did.

* The **x-axis** is the real spending values (actual values from the data).
* The **y-axis** is what my model predicted.
* Each dot is one prediction.
* If all the dots were perfectly on the diagonal line, the model would be 100% accurate.

As you can see, most of the points are really close to that line which means the model did a **pretty good job** at predicting spending!

## Contributing
Contributions are very welcome! Please fork the repository and create a pull request with your improvements.

## Contact
For questions or feedback, please open an issue in the repository or send an email to niserijemosope@gmail.com.
