# Monte Carlo Predictive Model: Geometric Brownian Motion

## Objective
This project engineers a Monte Carlo simulation engine to forecast continuous asset price trajectories over a 252-day trading horizon. The objective is to move beyond single-line deterministic predictions and model the expanding probability cone of an asset utilising Geometric Brownian Motion (GBM).

## Methodology & Technical Stack
The model leverages vectorisation to calculate 1,000 alternative future states, thereby bypassing computational bottlenecks.
* **Language:** Python 3
* **Mathematical Operations:** `numpy` (Vectorised random shock generation, logarithmic returns, percentile extraction)
* **Data Structuring:** `pandas` 
* **Visualisation:** `matplotlib` (Rendering the 100-path stochastic subset)

## Key Execution Steps
1. **Parameter Initialisation:** Established baseline metrics including Initial Price ($100), Annual Drift (5%), and Annual Volatility (20%).
2. **Stochastic Engine:** Generated a 252 x 1000 matrix of randomised daily returns utilising standard normal distribution and the GBM formula.
3. **Cumulative Trajectory:** Iterated the stochastic shocks over time to build continuous, compounding price paths.
4. **Statistical Extraction:** Analysed the terminal row of the matrix to extract the absolute mean and the 90% Confidence Interval.

## Output & Market Application
* **Mean Expected Price:** $105.16
* **90% Confidence Interval:** $73.93 — $144.07
This architecture mirrors the exact computational mechanics used in both particle physics (neutron diffusion modelling) and quantitative finance (derivatives pricing and risk assessment). By analysing the aggregate distribution of 1,000 simulated futures, this model defines the explicit mathematical boundaries of risk.
