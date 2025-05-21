# Linear Regressions on Student Performance

This repository explores how factors such as hours studied, previous scores, extracurricular participation, sleep habits, and practice with sample question papers influence a computed **Performance Index**. The analysis is performed in a single Google Colab notebook using a custom Kaggle-derived dataset.

## Dataset

- **Source Base:** Adapted from [https://www.kaggle.com/datasets/lainguyn123/student-performance-factors).  
- **Features:**  
  - `Hours Studied` (numeric)  
  - `Previous Scores` (numeric)  
  - `Extracurricular Activities` (binary; Yes → 1, No → 0)  
  - `Sleep Hours` (numeric)  
  - `Sample Question Papers Practiced` (numeric)  
- **Target Variable:**  
  - `Performance Index` (numeric)

In preprocessing, the categorical **Extracurricular Activities** column is converted to binary:
```python
data['Extracurricular Activities'] = data['Extracurricular Activities'].map({'Yes': 1, 'No': 0})
```

## Project Structure
```text
Linear-Regressions-on-Student-Performance/
├── data/
│   └── student_performance.csv       # Dataset with features and Performance Index
└── Student_Performance_Linear_Regression.ipynb  
```

## Usage

1. **Open the notebook in Google Colab**  
   - Click **Open in Colab**.  
2. **Mount your Google Drive** (if needed) and upload `student_performance.csv` into the `/content/data/` folder.  
3. **Run all cells** to execute data loading, preprocessing, linear regression training, and evaluation.  
4. **Inspect outputs:**  
   - Model metrics (R², MAE, MSE)  
   - Residual plots and feature coefficient analysis  

---

## Key Findings

- **Top Predictors:** Hours Studied, Previous Scores, and Extracurricular Activities  
- **Model Performance:** R² ≈ 0.65 on test splits  
- **Insights:** Residual analysis suggests exploring feature transformations or regularization for improved fit  
