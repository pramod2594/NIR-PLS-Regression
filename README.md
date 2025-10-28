# 🌾 NIR PLS Regression Pipeline

This project provides a complete **preprocessing and modeling pipeline** for Near-Infrared (NIR) spectral analysis using **Partial Least Squares (PLS) Regression**.  
It enables accurate prediction of multiple target properties (e.g., Protein, Fat, Moisture) from NIR spectra through systematic preprocessing, outlier detection, and regression modeling.

---

## 📘 Overview

The pipeline performs the following key steps:

1. **Preprocessing**
   - Baseline correction using Savitzky–Golay filter  
   - Normalization and vector normalization  
   - First derivative transformation  
   - Z-score based outlier detection and removal  

2. **Modeling**
   - Partial Least Squares (PLS) regression  
   - 5-fold cross-validation for performance evaluation  

3. **Evaluation Metrics**
   - **R²** – Coefficient of Determination  
   - **RMSECV** – Root Mean Square Error of Cross-Validation  
   - **RPD** – Residual Prediction Deviation  

4. **Visualization**
   - Predicted vs. True plots for each target variable  
   - 1:1 reference line for performance comparison  

---

## ⚙️ Requirements

Install all required libraries before running the notebook:

```bash
pip install numpy pandas scikit-learn scipy matplotlib openpyxl
```

---

## 🚀 Usage

1. Open the notebook in Jupyter:
   ```bash
   jupyter notebook NIR_PLS_Regression.ipynb
   ```

2. Update the configuration section with:
   - The first and last spectral column names  
   - The list of target columns to predict  

3. Run all cells to:
   - Preprocess spectra  
   - Remove outliers  
   - Train the PLS model for each target  
   - Display evaluation metrics and prediction plots  

---

## 📊 Output

- **Console results:**  
  Displays R², RMSECV, and RPD for each target variable.  
- **Plots:**  
  Shows Predicted vs. True scatter plots with a red dashed ideal-fit line.  

---

## 🧩 Customization

- Change the number of PLS components in the configuration:
  ```python
  pls_model = PLSRegression(n_components=5)
  ```
- Extend the pipeline for additional targets or preprocessing techniques.

---

## 🧠 Author

**Pramodha M.**  
*Data Analysis and Machine Learning for NIR Spectroscopy*

---

## 📄 License

This project is released under the [MIT License](LICENSE).
