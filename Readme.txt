# Breast Cancer Data Analysis Project

## Overview
This project analyzes a breast cancer dataset to explore and preprocess the data for potential machine learning tasks. The dataset contains various features related to breast cancer patients, such as age, race, tumor characteristics, and survival outcomes. The primary goal is to prepare the data by converting categorical variables into numerical formats suitable for modeling.

---

## Dataset

The dataset used in this project is sourced from a CSV file (`Breast_Cancer.csv`). It includes **4,024 entries** with **16 columns**, comprising both numerical and categorical data.

### **Numerical Features:**
- Age  
- Tumor Size  
- Regional Node Examined  
- Regional Node Positive  
- Survival Months  

### **Categorical Features (converted to numerical):**
- Race  
- Marital Status  
- T Stage  
- N Stage  
- 6th Stage  
- Differentiate  
- Grade  
- A Stage  
- Estrogen Status  
- Progesterone Status  
- Status (target variable: Alive or Dead)

---

## Project Structure

The project is implemented in a Jupyter Notebook (`breast-cancer.ipynb`) with the following key steps:

### **1. Data Loading**
- Dataset is loaded using `pandas` from `/kaggle/input/breast-cancer/Breast_Cancer.csv`
- Initial exploration includes viewing the first five rows and dataset info

### **2. Data Preprocessing**
- Categorical columns are encoded into numerical values using `sklearn.preprocessing.LabelEncoder`
- Transformed dataset contains only integer (`int64`) columns, verified via `data.info()`

### **3. Data Copy**
- A copy of the preprocessed dataset (`data2`) is created for additional analysis

### **4. Exploratory Data Analysis (EDA)**
- A profiling report is generated to summarize dataset characteristics (output not detailed in the notebook)

---

## Dependencies

The project relies on the following Python libraries:

- `numpy`: For numerical operations  
- `pandas`: For data manipulation and loading  
- `matplotlib.pyplot`: For potential plotting (not used in provided code)  
- `sklearn.preprocessing.LabelEncoder`: For encoding categorical variables  

> These libraries are pre-installed in the Kaggle environment used for this project.

---

## How to Run

### **Environment Setup**
- Ensure a Python environment with the required libraries installed  
- Alternatively, use a Kaggle notebook or a similar platform with the dataset and dependencies

### **Dataset**
- Place `Breast_Cancer.csv` in the appropriate directory (e.g., `/kaggle/input/breast-cancer/`)  
- Or update the file path in the notebook accordingly

### **Execution**
- Open `breast-cancer.ipynb` in Jupyter or any compatible environment  
- Run all cells sequentially to load, preprocess, and explore the data

---

## Outputs

- **Preprocessed Dataset**: Fully numerical and ready for ML tasks  
- **Data Insights**: Basic structure and type info via `data.info()`  
- **Profiling Report**: HTML-based summary report (dependent on `pandas-profiling`)

---

## Future Work

- **Feature Selection**: Identify most relevant predictors for the `Status` variable  
- **Modeling**: Apply classification models to predict patient outcomes  
- **Visualization**: Use plots to examine relationships between features and survival status  
- **Advanced EDA**: Deeper statistical analysis of distributions and correlations

---

## Notes

- The notebook assumes a Kaggle environment (based on file paths and imports)  
- `Status` (encoded as 0 or 1) likely represents patient survival (Alive or Dead)  
- Profiling report generation outside Kaggle may require `pandas-profiling` or similar packages

---

## License

This project is for educational purposes and uses a publicly available dataset. Ensure compliance with any dataset-specific licensing terms when using or sharing the data.
