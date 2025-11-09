# Assignment for Research and Development / AI  
## Parametric Curve Parameter Estimation

This project focuses on identifying three hidden parameters from a dataset of
points sampled along a curve. The dataset (`xy_data.csv`) contains points
generated from a parametric model where three variables were intentionally left
unknown:

- The rotation angle (theta)  
- The exponential growth/decay factor (M)  
- A horizontal shift value (X)

The assignment requires estimating these three variables within specific ranges:

- Theta is between 0° and 50°  
- M is between -0.05 and 0.05  
- X is between 0 and 100  
- The parameter t runs from 6 to 60

The goal is to find the values of theta, M, and X that best reproduce the
original curve from the dataset.

---

## ✅ Final Estimated Parameters

After analysis and curve fitting, the parameters that best match the provided
data are:

- **Theta = 30°**  
- **M = 0.03**  
- **X = 55**

These values recreate the curve extremely accurately when applied back into the
parametric model.

---

## ✅ Desmos Visualization

To help visualize the final curve, a Desmos graph is available here:

**Desmos link:**  
https://www.desmos.com/calculator/pwda0nktb1

This link plots the final curve using the recovered parameters and shows how
closely it matches the original point data.

---

## 📁 Repository Contents

- `README.md` — This file  
- `solve.md` — Explanation of how the parameters were estimated (plain English)  
- `xy_data.csv` — The provided dataset  
- (Optional) `fit.py` — Python script used for solving

---

## ✅ Summary

This project demonstrates how hidden parameters in a parametric model can be
recovered from real data using numerical methods and visualization tools.  
The recovered values match the original curve with near-perfect accuracy.
