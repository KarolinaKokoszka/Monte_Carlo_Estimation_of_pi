# Monte_Carlo_Estimation_of_pi
This project demonstrates how to estimate the value of π (pi) using the Monte Carlo method, a simple and powerful technique based on random sampling.

## 📌 How It Works

The idea is to simulate random points inside a unit square and count how many fall within a quarter circle of radius 1. The proportion of points that fall inside the circle gives an approximation of π.

### Estimation Formula:
\[
\pi \approx 4 \times \frac{\text{Number of points inside quarter circle}}{\text{Total number of points}}
\]

### Algorithm Steps:
1. Randomly generate `N` (x, y) points in the range \([0, 1] \times [0, 1]\).
2. Check if a point lies inside the quarter circle using the condition:
   \[
   y \leq \sqrt{1 - x^2}
   \]
3. Count the points inside and outside the circle.
4. Estimate π after each point using the formula above.
5. Store and visualize the results.

## 📊 Visualizations

The project generates the following plots:

### 1. Scatter Plots for Different N
For values `N = [100, 1000, 10000, 100000]`, scatter plots are created showing:
- Blue points: Inside the quarter circle.
- Red points: Outside the circle.
- A black arc representing the true boundary of the quarter circle.

### 2. π Estimation Path
A line plot that tracks how the π estimate evolves with the number of points. As `N` increases, the estimation stabilizes near the actual value of π.

### 3. Repeated Experiments
For each value of `N`, the estimation experiment is repeated 10 times. Each run is visualized to show the effect of randomness on the estimate. Larger `N` results in less variation between runs.

### 4. Statistical Analysis (Boxplots)
Boxplots show the distribution of π estimates across 10 runs for each value of `N`. This highlights:
- Greater spread for small `N`
- More accurate and consistent estimates for larger `N`

## 🔍 Observations

- **Convergence:** The larger the number of points, the closer the estimate gets to the true value of π.
- **Randomness Impact:** Small values of `N` produce high variance in results; repeated experiments help reveal this.
- **Statistical Insights:** Boxplots illustrate how estimate variance decreases as `N` increases.

## ✅ Summary

Monte Carlo is an effective and intuitive method to estimate π. While it's not the most efficient algorithm for high precision, it's a great example of probabilistic numerical methods. Accuracy improves with more samples, showcasing the Law of Large Numbers in practice.
