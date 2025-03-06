# Predictive Modeling of Solid Holdup Distribution in Fluidized Chemical Reactors Using Machine Learning Algorithms

This project demonstrates the use of five different machine learning algorithms to predict the solids holdup distribution in Liquid-Solid Circulating Fluidized Bed (LSCFB) reactors. The objective is to model reactor hydrodynamics accurately using experimental data, thereby reducing the need for expensive and hazardous experiments.

---

## 1. Background
In this work, five different machine learning algorithms are utilized to predict the solids holdup distribution in three LSCFB reactors and to model their hydrodynamics. LSCFB reactors are essential in chemical, biochemical, environmental, and petrochemical applications. However, experimental studies on these reactors can be prohibitively expensive and sometimes impractical due to safety and technical limitations. Machine learning offers an efficient alternative to capture complex reactor behaviors with reduced cost and risk.

---

## 2. Data Collection
Experimental data were manually collected from two LSCFB systems:
- **Razzak system** (Razzak et al., 2020)
- **Zheng system** (Zheng et al., 2002)

The dataset includes a range of operating conditions across various radial and axial positions, with the following parameters:
- **Us:** Superficial solids velocity (cm/s)
- **Ul:** Superficial liquid velocity (cm/s)
- **Ut:** Terminal settling velocity (cm/s)
- **D:** Diameter of the particles (µm)
- **x:** Axial location (m)
- **x/L:** Dimensionless axial position
- **r/R:** Dimensionless radial position

The target is to predict the experimental solids holdup distribution—a key factor that affects hydrodynamics, mass transfer, and reactor performance.

---

## 3. Data Cleaning
The dataset is provided in the file `Solid_Holdup.csv`. Data cleaning steps include:
- Handling missing values and outliers.
- Standardizing and normalizing parameters.
- Ensuring data consistency for accurate model training.

---

## 4. Deploying Machine Learning Models
The predictive models are implemented in the Jupyter Notebook `Solid_Holdup_Distribution_Predictive_Model.ipynb`. The following regression models are deployed:

### 4.1 Linear Regression
- **Overview:** Assumes a linear relationship between features and the target.
- **Usage:** Serves as a baseline model.

### 4.2 K-Nearest Neighbors Regression (KNN)
- **Overview:** Predicts outcomes based on the average of the nearest neighbors.
- **Usage:** Sensitive to local data structures and noise.

### 4.3 Support Vector Machine Regression (SVM)
- **Overview:** Uses SVMs to capture non-linear relationships through kernel methods.
- **Usage:** Performance depends on proper kernel and hyperparameter tuning.

### 4.4 Decision Tree Regression (DTR)
- **Overview:** Uses decision trees to model complex, non-linear relationships.
- **Usage:** Can overfit if not properly pruned, yet captures data intricacies.

### 4.5 Random Forest Regression (RFR)
- **Overview:** An ensemble method combining multiple decision trees to improve generalization.
- **Usage:** Demonstrates superior performance by reducing overfitting and capturing non-linear patterns.

---

## 5. Comparing the Models
Performance was evaluated using metrics such as Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R² score:

- **Random Forest Regression (RFR):**  
  - MSE: 0.000018  
  - R²: 0.987348  
  - RMSE: 0.004237  
  *Best performance due to its ensemble approach.*

- **Decision Tree Regression (DTR):**  
  - R²: 0.979848  
  - MSE: 0.000029  
  *Strong performance but may be prone to overfitting.*

- **Support Vector Machine Regression (SVM)** and **Linear Regression (LR):**  
  - Moderate performance with R² scores around 0.79 and MSE values near 0.000296–0.000299.  
  *Limited by their inherent assumptions.*

- **K-Nearest Neighbors Regression (KNN):**  
  - R²: 0.704849  
  - RMSE: 0.020465  
  *Lowest performance, indicating challenges in capturing complex non-linear relationships.*

---

## 6. Discussion and Conclusion
The analysis confirms that Random Forest Regression (RFR) is the most effective model for predicting solids holdup distribution in LSCFB reactors. Its ensemble nature allows it to capture intricate non-linear relationships, resulting in high predictive accuracy. Although Decision Tree Regression (DTR) also performs well, its susceptibility to overfitting makes it less reliable than RFR. The simpler models (Linear Regression and KNN) underperform, highlighting the necessity for advanced methods when dealing with complex hydrodynamic phenomena.

---

## 7. How to Run

### Data Preparation:
Ensure that the `Solid_Holdup.csv` file is present in the repository root.

### Notebook Execution:
Open `Solid_Holdup_Distribution_Predictive_Model.ipynb` using Jupyter Notebook or JupyterLab.

### Run the Analysis:
Execute the notebook cells sequentially to perform data cleaning, model training, evaluation, and model comparison.

---

## 8. Modeling Results Snapshot
Below is a snapshot of the modeling results showcasing key performance metrics.


![Image 3](https://github.com/user-attachments/assets/cbf85e92-d9ff-4f37-85de-12438e48b39a)

*Figure: Comparison of model performance metrics (MSE, RMSE, R²)*

---

## 9. References
- **Zheng, Y., Zhu, J.-X., Marwaha, N. S., & Bassi, A. S.** (2002). Radial solids flow structure in a liquid–solids circulating fluidized bed. *Chemical Engineering Journal, 88*(1), 141-150.
- **Razzak, S. A., Al-Hammadi, S. A., Rahman, S. M., Quddus, M. R., Hossain, M. M., & Zhu, J.** (2020). Scale-up effect analysis and modeling of liquid–solid circulating fluidized bed risers using multigene genetic programming. *Particuology, 52*, 57-66.

---

## 10. Repository Structure
```bash
├── README.md
├── Solid_Holdup.csv
└── Solid_Holdup_Distribution_Predictive_Model.ipynb
