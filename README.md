
# Final Project: Unlocking Customer Behavior for Effective Marketing

### Team: Data Enthusiasts  
**Team Members**: Amanullah (Leader) & Daniyal Hyder  
**Assigned By**: Miss Reema Memon  

---

## Project Overview

In today’s data-driven digital world, understanding customer behavior is essential for effective marketing strategies. This project focuses on analyzing engagement data, loyalty points, and campaign metrics to answer key marketing questions, evaluate channel performance, and predict customer conversion.

**Key Objectives**:
1. Identify customers at risk of leaving.
2. Segment customers for targeted marketing strategies.
3. Evaluate the effectiveness of Social Media and PPC campaigns.
4. Assess overall marketing channel effectiveness.
5. Develop classification models to predict customer conversion.

---

## Dataset Overview

**Name**: Digital Marketing Dataset  
**Source**: Kaggle  
**Size**: 2000 rows x 20 columns  

### Features

#### **Demographic Information**:
- `CustomerID`: Unique customer identifier.
- `Age`: Customer's age.
- `Gender`: Male/Female.
- `Income`: Annual income in USD.

#### **Marketing-Specific Variables**:
- `CampaignChannel`: Marketing channel (e.g., Email, Social Media).
- `CampaignType`: Campaign purpose (e.g., Awareness, Conversion).
- `AdSpend`: Marketing spend in USD.
- `ClickThroughRate`: Customer click rate on ads.
- `ConversionRate`: Ratio of clicks converting to desired actions.

#### **Customer Engagement Variables**:
- `WebsiteVisits`: Visits to the website.
- `PagesPerVisit`: Pages visited per session.
- `TimeOnSite`: Time spent on the website (minutes).
- `SocialShares`: Shares on social media.
- `EmailOpens` & `EmailClicks`: Email interaction metrics.

#### **Historical Data**:
- `PreviousPurchases`: Number of past purchases.
- `LoyaltyPoints`: Accumulated loyalty points.

#### **Target Variable**:
- `Conversion`: Binary variable indicating customer conversion.

---

## Methodology

### Data Preprocessing
1. **Standardization**: Unified column names and formats.
2. **Missing Values**: No missing data found.
3. **Column Removal**:
   - `CustomerID`: Identifier only.
   - `AdvertisingPlatform` & `AdvertisingTool`: Non-predictive.
4. **Outlier Detection**: No significant outliers detected.

### Feature Engineering
- **Total Page Views**: Combined `WebsiteVisits` & `PagesPerVisit`.
- **Email Engagement**: Unified `EmailOpens` & `EmailClicks`.
- **Gender Encoding**: Converted to binary (Male = 0, Female = 1).

---

## Analysis & Findings

### Key Problems Addressed

1. **Identifying At-Risk Customers**:
   - **Results**: 4164 out of 8000 customers identified as at risk.

2. **Customer Segmentation**:
   - **Segments**: 
     - **Segment 0**: High engagement, low conversion.
     - **Segment 1**: Responsive to marketing (high click-through rates).
     - **Segment 2**: High conversion readiness.

3. **Hypothesis Testing (Social Media vs. PPC)**:
   - **Result**: No significant difference in conversion rates (p-value = 0.2150).

4. **Marketing Channel Effectiveness**:
   - **Top Performers**: Social Media for both CTR and conversion rate.

5. **Predictive Modeling**:
   - **Features Used**: `TotalPageViews`, `TimeOnSite`, `AdSpend`, etc.
   - **Best Model**: Gradient Boosting (90.38% accuracy post-tuning).

### Models & Accuracy
| Model                 | Pre-Tuning Accuracy | Post-Tuning Accuracy |
|-----------------------|---------------------|----------------------|
| Gradient Boosting     | 89.94%             | **90.38%**          |
| Random Forest         | 89.31%             | 89.19%              |
| Decision Tree         | 81.06%             | 88.50%              |
| Neural Network (MLP)  | 17.81%             | 87.88%              |
| SVM (RBF Kernel)      | 54.69%             | 87.88%              |
| K-Nearest Neighbors   | 62.88%             | 87.75%              |

---

## Tools & Libraries

- **Data Handling**: Pandas (v2.2.2), NumPy (v1.26.4)
- **Visualization**: Matplotlib (v3.8.0), Seaborn (v0.13.2), Plotly (v5.24.1)
- **Machine Learning**: Scikit-Learn (v1.5.2), XGBoost, TensorFlow (v2.17.0)
- **Statistical Analysis**: Statsmodels, Scipy

---

## Future Work

1. **Streamlit Web App**:
   - Real-time predictions for customer conversion.
   - Interactive segmentation visualization.

2. **Advanced Modeling**:
   - Regression models for precise conversion rate prediction.
   - Deep learning exploration with TensorFlow or PyTorch.

3. **Marketing Optimization**:
   - Personalized recommendations based on segmentation insights.

---

## Acknowledgments

Special thanks to **Miss Reema Memon** for her guidance, **Gexton** and **PITP management** for their support, and the **Kaggle community** for providing high-quality data.

---

## Resources
- [Colab Notebook](https://colab.research.google.com/drive/1dPsFX37MUN0C7n1o5-TJrUYdYYSbpYTg?usp=sharing)  
- [GitHub Repository](https://github.com/Amanullahmemon75/final_project_of_PITP)  

---

