# **Sales Prediction Analysis with Linear Regression**

## **Project Overview**
This project employs **Linear Regression** to model and forecast sales based on advertising expenditures across TV, radio, and newspaper channels. The analysis identifies key drivers of sales, evaluates model performance, and provides actionable business insights to optimize marketing spend.

---

## **Key Deliverables**
✔ **Exploratory Data Analysis (EDA)** - Statistical summaries and visual relationships between ad spend and sales  
✔ **Feature-Target Correlation** - Quantified impact of each marketing channel on sales performance  
✔ **Multivariate Regression** - Predictive modeling using all features (TV, radio, newspaper)  
✔ **Model Comparison** - Performance evaluation of models with:  
   - **TV-only**  
   - **TV + Radio**  
   - **All features**  
✔ **Performance Metrics** - R², RMSE, and cross-validation to validate prediction accuracy  

---

## **Data Visualization & Insights**

### **1. Feature-Target Relationship**
<img width="949" height="390" alt="feature_target_pairplot" src="https://github.com/user-attachments/assets/cf2f8c9a-bdfc-4daa-8afe-4a29b54dbe71" />

- **TV advertising** shows the strongest linear correlation with sales (R² = 0.797)  
- **Radio** exhibits complementary effects when combined with TV  
- **Newspaper** shows minimal impact on sales  

### **2. Model Performance Comparison**
#### **All Features Model (TV + Radio + Newspaper)**
<img width="465" height="391" alt="act_vs_pred(all features)" src="https://github.com/user-attachments/assets/6c585027-a6e4-4c52-9e42-533cd5efbd9b" />
  
- **R²: 0.912** - Explains 91.2% of sales variance  
- **RMSE: 1.551** - Average prediction error of $1,551  
- **Cross-Val R²: 0.892** - Consistent performance  

## **TV & Radio Model**
##<img width="465" height="391" alt="act_vs_pred(tv_radio)" src="https://github.com/user-attachments/assets/6b1b2e31-ac1a-47eb-9a51-3d3442e38639" />

- **R²: 0.913** - Marginally better than full model  
- **RMSE: 1.535** - Slightly improved accuracy  
- **Cross-Val R²: 0.892** - Robust generalization  

#### **TV Only Model**
<img width="465" height="391" alt="act_vs_pred(tv)" src="https://github.com/user-attachments/assets/d4cb8e3d-7f13-4dd1-8f2a-e7861c6defb7" />

- **R²: 0.797** - Explains 79.7% of variance  
- **RMSE: 2.348** - Larger prediction errors  
- **Cross-Val R²: 0.892**  

---

## **Key Findings**
1. **TV advertising is the dominant sales driver** (accounts for 79.7% of explainable variance)  
2. **Radio provides significant complementary value** - Adding radio to TV model improves R² from 0.797 to 0.913  
3. **Newspaper ads show negligible impact** - Inclusion doesn't improve model performance  
4. **Optimal Model**: TV + Radio (Highest R² and lowest RMSE)  

---

## **Business Recommendations**
 - Reallocate the newspaper budget to TV and radio for maximum ROI  
 - Maintain TV as primary channel but explore optimal spending levels  
 - Leverage radio's complementary effect through coordinated campaigns  
 - Consider testing** radio ad variations and daypart strategies  


## **Technical Implementation**
### **Tools Used**
- **Python**: Pandas (data processing), Scikit-learn (modeling), Matplotlib/Seaborn (visualization)  
- **Statistical Methods**: OLS Regression, 5-fold Cross-Validation  

### How to Reproduce
1. Clone the repository:  
   ```bash  
   git clone [repo-url]  
   ```  
2. Install dependencies:  
   ```bash  
   pip install pandas scikit-learn matplotlib seaborn  
   ```  
3. Run the Jupyter Notebook:  
   ```bash  
   jupyter notebook sales_analysis.ipynb  
   ```  

---

## **Future Enhancements**
- Test **non-linear relationships** (polynomial features)  
- Incorporate **interaction terms** (TV × Radio)  
- Apply **regularization techniques** for potential overfitting  
- Expand dataset with **seasonal variables**  


📊 **For detailed analysis, refer to the code and visualizations in the notebook.**  

*Note: All monetary values are in thousands (e.g., RMSE of 1.551 = $1,551)*
