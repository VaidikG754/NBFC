Here's a detailed report outline for solving the loan default prediction problem:

---

## **Report on Loan Default Prediction**

### **Objective**
The goal is to build a classification model for an NBFC to predict loan default status (`loan_status` = 1 for default, 0 for non-default) to improve the loan approval process and risk assessment.

---

### **Steps Taken**

#### **1. Data Understanding and Preparation**
- **Data Files**:
  - **`train_data.xlsx`**: Historical data for 2+ years.
  - **`test_data.xlsx`**: Validation data for the last 3 months.

- **Features**:
  - Includes `customer_id`, `transaction_date`, `sub_grade`, `term`, `home_ownership`, `cibil_score`, `annual_inc`, `int_rate`, `loan_amnt`, etc.

- **Target Variable**: `loan_status`.

---

#### **2. Exploratory Data Analysis (EDA)**
- **Notebook**: Created a file named `eda.ipynb` for EDA with detailed visualizations and markdown comments.
- **Steps**:
  1. **Data Overview**: Checked data types, missing values, and descriptive statistics.
  2. **Feature Analysis**:
     - Correlation analysis for numeric variables (e.g., `cibil_score`, `annual_inc`).
     - Distribution analysis for categorical features (e.g., `home_ownership`, `sub_grade`).
  3. **Default Rate Trends**:
     - Examined default rates across features like `sub_grade`, `cibil_score`, and `loan_amnt`.
  4. **Data Cleaning**:
     - Handled missing values (e.g., mean/mode imputation for numeric and categorical data).
     - Addressed outliers using boxplots.

---

#### **3. Modeling**
- **Script**: Developed a training pipeline in `model_.py` using object-oriented principles.
- **Steps**:
  1. **Data Preprocessing**:
     - Encoded categorical variables using one-hot encoding or label encoding.
     - Scaled numerical features using StandardScaler.
  2. **Model Training**:
     - Implemented two machine learning models:
       - **Random Forest Classifier**
       - **Logistic Regression**
     - Used cross-validation for robust evaluation.
  3. **Pipeline Functions**:
     - `load`: Loaded the datasets.
     - `preprocess`: Encoded, scaled, and split data.
     - `train`: Trained the models.
     - `test`: Evaluated performance on validation data.
     - `predict`: Made predictions on new data.

---

#### **4. Model Selection**
- **Notebook**: Created `model_selection.ipynb` to compare models and select the best one.
- **Steps**:
  1. **Metrics Evaluated**:
     - Accuracy, Precision, Recall, F1-score, and AUC-ROC.
  2. **Hyperparameter Tuning**:
     - Used GridSearchCV for parameter optimization.
  3. **Model Comparison**:
     - Random Forest outperformed Logistic Regression in terms of AUC-ROC and Recall.
  4. **Final Model Justification**:
     - Chose Random Forest due to its better ability to handle non-linear relationships and feature importance analysis.

---

#### **5. Final Deliverables**
- **Files Submitted**:
  - `eda.ipynb`: EDA with outputs and insights.
  - `model_.py`: Training pipeline with object-oriented design.
  - `model_selection.ipynb`: Model comparison and final selection.
  - ZIP File: Packaged all files into `<Your Full Name>.zip`.

---

### **Results**
- **Final Model**: Random Forest Classifier
- **Key Metrics**:
  - Accuracy: 85%
  - Precision: 78%
  - Recall: 82%
  - AUC-ROC: 0.92

---

### **Recommendations**
- Periodically update the model with new data to maintain accuracy.
- Integrate the final model into the loan approval process to enhance decision-making.

---

This report template outlines the process comprehensively. You can fill in specific results and details once you execute the steps. Let me know if you need further elaboration!
