# **Telco Customer Churn Prediction Project**

## **What's This About?**
This project looks at why telecom customers leave (we call this "churn") and tries to predict who might leave next. I used machine learning to find patterns and figure out what really makes customers stay or go.


## **What I Did**
**Explored the data** - Looked at different customer groups and their churn patterns  
**Found key patterns** - Discovered what factors most affect churn  
**Built a prediction model** - Created a tool that can flag at-risk customers using Random Forest 
**Came up with ideas** - Thought of ways the company could keep more customers  


## **Things I Found**

### **1. Who's Leaving?**
 <img width="580" height="455" alt="Churn Distribution" src="https://github.com/user-attachments/assets/0c182cdd-11a7-4cf1-92fe-040766c86f8e" />

- Most customers stick around (about 73%)  
- But we still want to save those who might leave!  

### **2. Contracts Matter A Lot**
<img width="580" height="455" alt="C_T vs Churn" src="https://github.com/user-attachments/assets/5e9990d0-80e3-4cfe-920e-5bbae94074e8" />

- Month-to-month customers leave 3x more often than yearly contract customers  
- This was the biggest predictor of churn  

### **3. What Else Affects Churn?**
<img width="638" height="435" alt="Important features" src="https://github.com/user-attachments/assets/e9e79854-8b60-42f1-a796-48a630effd3b" />

**Top Things That Keep Customers:**  
1. How long they've been with the company  
2. Having online security  
3. Tech support access  
4. Payment method choices  


## **What The Company Could Do**
**Make longer contracts more appealing** - Maybe offer discounts  
**Bundle important services** - Like security and tech support  
**Check prices** - Some plans might be too expensive  
**Help month-to-month customers** - Maybe special offers and discounts for them  


## **How I Did It**
- Used **Python** with pandas and scikit-learn  
- Built a **Random Forest model** (it worked pretty well!)  
- Got these scores:  
  - 82% precision (when it says someone will leave, it's usually right)  
  - 52% recall (catches about half of actual leavers)  

To run it yourself:
```bash
git clone [repo-url]
pip install -r requirements.txt
jupyter notebook churn_analysis.ipynb
```

## **What Could Be Better Next Time**
- Try using **more customer data** like service calls  
- Test **other machine learning methods**  
- Build a **real-time warning system**  


This was a really interesting project! It showed me how data science can help solve real business problems. The company could actually use these findings to keep more customers happy. 😊

*P.S. All numbers are based on my analysis of the dataset*
