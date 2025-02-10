# Predictive Modeling of Solid Holdup Distribution in Fluidized Chemical Reactors Using Machine Learning Algorithms

## Project Overview
This project explores the use of five machine learning algorithms to predict the **solids holdup distribution** in three **Liquid-Solid Circulating Fluidized Bed (LSCFB) reactors**. These reactors are crucial in **chemical, biochemical, environmental, and petrochemical industries**.

Traditional experimental methods to study LSCFB hydrodynamics are **costly, resource-intensive, and sometimes impractical** due to safety concerns. Machine learning offers a promising alternative to **model reactor behavior accurately** while reducing reliance on experimental setups.

## Data Collection
The dataset for this project was gathered manually from two key LSCFB reactor studies:
- **Razzak System** (Razzak et al., 2020)
- **Zheng System** (Zheng et al., 2002)

The dataset includes a wide range of **operating conditions**, covering multiple **radial and axial positions** and various **fluidization parameters**.

## Model Parameters
The machine learning models were trained using the following parameters:

| Parameter | Description |
|-----------|-------------|
| **Us** | Superficial solids velocity (cm/s) |
| **Ul** | Superficial liquid velocity (cm/s) |
| **Ut** | Terminal settling velocity (cm/s) |
| **D**  | Particle diameter (µm) |
| **x**  | Axial position (m) |
| **x/L** | Dimensionless axial position |
| **r/R** | Dimensionless radial position |

## Target Variable
The goal is to predict **solids holdup distribution**, which represents the fraction of the **reactor volume occupied by solid particles** in the liquid phase. This parameter significantly influences **hydrodynamics, mass transfer, and overall reactor performance**.

## Machine Learning Approach
The study evaluates **five machine learning algorithms**, training them on experimental data to develop models that can accurately represent fluidized bed reactor behavior.

## References
- Zheng, Ying, Jing-Xu Zhu, Narenderpal S. Marwaha, and Amarjeet S. Bassi.  
  **"Radial solids flow structure in a liquid–solids circulating fluidized bed."**  
  *Chemical Engineering Journal* 88, no. 1 (2002): 141-150.  

- Razzak, Shaikh A., Saddam A. Al-Hammadi, Syed M. Rahman, Mohammad R. Quddus, Mohammad M. Hossain, and Jesse Zhu.  
  **"Scale-up effect analysis and modeling of liquid–solid circulating fluidized bed risers using multigene genetic programming."**  
  *Particuology* 52 (2020): 57-66.  



