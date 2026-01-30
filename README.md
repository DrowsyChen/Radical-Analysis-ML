# Radical-Analysis-ML
Implementation of tree-based ensemble models (Random Forest, XGBoost, and GBDT) for chemical radical analysis, supporting manuscript NCOMMS-25-448078.

## 1. System Requirements
### Software Dependencies
The code is developed in Python and requires the following libraries:
* **Python** (version 3.8 or higher)
* **Data Handling**: pandas, numpy, openpyxl
* **Machine Learning**: scikit-learn, xgboost, shap
* **Visualization**: matplotlib, seaborn

### Operating Systems
This software has been tested on **Windows 10/11**, **macOS (Intel/M1)**, and **Linux (Ubuntu 20.04+)**. 

### Hardware Requirements
No non-standard hardware is required; the scripts run efficiently on standard desktop or laptop computers.

## 2. Installation Guide
### Instructions
1. **Environment**: We recommend using an [Anaconda](https://www.anaconda.com/) environment.
2. **Setup**: Install the required packages via pip:
```
pip install pandas numpy scikit-learn xgboost shap matplotlib seaborn openpyxl
```

### Typical Install Time
The installation of dependencies on a "normal" desktop computer typically takes 2–5 minutes.

## 3. Demo
**Instructions to Run**
1. Ensure Radical_Analysis.xlsx is in the same directory as the notebooks.
2. Open Jupyter Notebook (via Anaconda or Command Prompt).
3. Run all cells in GBDT_Analysis.ipynb, RF_Analysis.ipynb, or XGBoost_Analysis.ipynb.

**Expected Output**  
Successful execution will generate:
* Model Metrics: $R^2$ and $RMSE$ scores printed in the notebook.
* Visualizations: Feature importance bar charts, SHAP summary plots, and hyperparameter sensitivity heatmaps.

**Expected Run Time**  
The complete training and evaluation demo (including GridSearch) takes approximately 5–10 minutes on a standard desktop.

## 4. Instructions for Use
**Running on Your Own Data**  
To apply these models to a custom dataset:
1. Format your data as an .xlsx file mirroring the structure of Radical_Analysis.xlsx.
2. Update the file_path variable and feature column names within the notebook to match your dataset.

## **Repository Structure**
* GBDT_Analysis.ipynb: Implementation and sensitivity analysis for GBDT.
* RF_Analysis.ipynb: Implementation and sensitivity analysis for Random Forest.
* XGBoost_Analysis.ipynb: Implementation and sensitivity analysis for XGBoost.
* Radical_Analysis.xlsx: The primary dataset used for training and testing.

## **Methodology Summary**
* Data Splitting: Randomly partitioned into training and testing sets to mimic real-world predictive scenarios.
* Leakage Prevention: Test data remains strictly isolated during hyperparameter optimization.
* Cross-Validation: 5-fold cross-validation is used during the model selection phase.
* Interpretability: Validated via SHAP values and feature importance to ensure physical significance.

## **License**
This project is licensed under the MIT License.
