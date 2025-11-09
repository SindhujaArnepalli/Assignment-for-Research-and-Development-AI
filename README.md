# Assignment-for-Research-and-Development-AI
# Parametric Curve Parameter Estimation

This repository contains the solution to the assignment of identifying the
unknown parameters \(\theta\), \(M\), and \(X\) in the following parametric
curve:

\[
x(t)=t\cos(\theta)-e^{M|t|}\sin(0.3t)\sin(\theta)+X
\]

\[
y(t)=42+t\sin(\theta)+e^{M|t|}\sin(0.3t)\cos(\theta)
\]

The dataset `xy_data.csv` contains a list of points sampled from this curve
for parameter values \(6 < t < 60\).

---

## ✅ Problem Overview

We're given:
- **Three unknown variables**:  
  - \(\theta\) (in degrees),  
  - \(M\),  
  - \(X\)

- **Parameter ranges**:  
  - \(0^\circ < \theta < 50^\circ\)  
  - \(-0.05 < M < 0.05\)  
  - \(0 < X < 100\)

- **Goal**: Estimate these parameters so that the curve matches the dataset with
minimum error.

The oscillatory term  
\[
e^{M|t|}\sin(0.3t)
\]  
creates a rotated, growing (or decaying) sinusoidal ripple on top of a straight,
tilted base line. Recovering the parameters requires aligning the dataset to
this model.

---

## ✅ Final Estimated Parameters

After solving the system using numerical optimization:

\[
\boxed{\theta = 30^\circ,\quad M = 0.03,\quad X = 55}
\]

These values reproduce the dataset with extremely low error.

---

## ✅ Final Parametric Curve (LaTeX)

\[
x(t)=t\cos(30^\circ)-e^{0.03|t|}\sin(0.3t)\sin(30^\circ)+55
\]

\[
y(t)=42+t\sin(30^\circ)+e^{0.03|t|}\sin(0.3t)\cos(30^\circ)
\]

---

## ✅ Viewing the Curve in Desmos

To visualize the curve, copy this **exact** Desmos-compatible expression:

