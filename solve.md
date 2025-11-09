# How the Parameters Were Found

This document explains in simple terms how the three unknown variables were
identified from the dataset.

---

## 1. Understanding the Problem

We were given a collection of points that all lie on a specific curve.  
The curve depends on three unknown values:

- A rotation angle  
- A growth/decay factor  
- A horizontal shift  

The task was to reverse-engineer these values from the points.

The dataset came with limits for each unknown, so we knew roughly where the
solution should be.

---

## 2. Strategy for Solving

Since the data points come from a smooth curve, the goal was to adjust the three
unknown values until the curve produced by those values lines up as closely as
possible with the data.

To do this:

1. A computer program was written to test different combinations of the three
   variables.
2. For each combination, the program measured how closely the predicted curve
   matched the actual data.
3. The program gradually adjusted the values to reduce the difference.
4. After many improvements, it arrived at a set of values that fit the curve
   extremely well.

This approach is known as numerical optimization.

---

## 3. Why the Solution Works

The reason this works is that the shape of the curve depends very sensitively on
the three unknown parameters. Even small changes in the values noticeably alter
the shape.

This means that when the program finds the one set of values that matches the
data almost perfectly, we can be confident that it has recovered the correct
parameters.

---

## 4. Final Result

The best-fit values of the three unknowns were:

- Rotation angle (theta): **30°**
- Growth/decay factor (M): **0.03**
- Horizontal shift (X): **55**

The resulting curve aligns with the data points extremely closely.

---

## 5. Visualization

A Desmos graph was created to verify this visually. The link is provided in the
main README. When loaded, the curve for the recovered parameters traces almost
exactly over the sampled data.

---

## 6. Conclusion

The three hidden values were successfully reconstructed using numerical
optimization and geometric insights. The approach is robust and replicable for
similar curve-reconstruction problems.
