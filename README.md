# Telecom Customer Churn Prediction and Segmentation

## Project Overview
This project applies Machine Learning techniques to analyze and predict customer churn for a telecommunications company. It involves extensive exploratory data analysis (EDA), predictive modeling using a Random Forest Classifier, and customer segmentation using K-Means clustering to identify different customer profiles.

## Dataset
* **File:** `Telco_customer_churn.xlsx` (or `.csv` equivalent)
* **Description:** The dataset contains customer demographic information, account details, subscribed services, and whether or not the customer churned. 

## Technologies & Libraries Used
* **Programming Language:** Python 3
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (`RandomForestClassifier`, `KMeans`, `StandardScaler`, `train_test_split`, classification metrics)

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
* Analyzed the distribution of tenure months and monthly charges.
* Investigated the relationship between tenure and churn using boxplots and histograms.

### 2. Data Preprocessing
* Handled redundant columns and dropped unnecessary features (e.g., `CustomerID`, `Country`, `State`, `Lat Long`, etc.).
* Performed One-Hot Encoding (`pd.get_dummies()`) to convert categorical variables into numerical format.
* Scaled features using `StandardScaler` for clustering.

### 3. Predictive Modeling (Churn Prediction)
* **Base Model:** Built a baseline `RandomForestClassifier`.
* **Handling Class Imbalance:** Applied `class_weight='balanced'` to improve recall for churned customers.
* **Hyperparameter Tuning:** Adjusted parameters like `n_estimators` and `max_depth` to optimize model performance.
* **Feature Importance:** Analyzed the top contributing features to customer churn (e.g., Tenure Months, Total Charges, Contract type).

### 4. Customer Segmentation (Clustering)
* Extracted specific features (`Tenure Months`, `Monthly Charges`, `Total Charges`, `Churn Probability`) for segmentation.
* Used the **Elbow Method** to determine the optimal number of clusters (k=3) for **K-Means Clustering**.
* Grouped customers into 3 actionable segments:
  * **Budget Loyal Customers**
  * **High Risk New Customers**
  * **Loyal Premium Customers**

## Key Results
* Successfully predicted churn with balanced accuracy using the tuned Random Forest model.
* Identified that `Tenure Months` and `Total Charges` are the most significant factors influencing churn.
* Segmented customers into distinct risk and value groups to help tailor retention strategies.

## How to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/just-aakash/churn-prediction-ml.git
   ```
2. Ensure you have Jupyter Notebook installed or open the `.ipynb` file in Google Colab.
3. Install the required dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
4. Place the `Telco_customer_churn.xlsx` dataset in the same directory as the notebook.
5. Run the cells in the `CBSOTSIP-ML-P1.ipynb` notebook.
