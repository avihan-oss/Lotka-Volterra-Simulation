# Predator-Prey Population Dynamics — Lotka-Volterra Simulation

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/avinash-chauhan-oss/Lotka-Volterra-Simulation/blob/main/notebooks/01_lotka_volterra_dynamics.ipynb)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![SciPy](https://img.shields.io/badge/Library-SciPy-8CAAE6.svg)](https://scipy.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()

Mathematical modeling and parameter fitting of the famous **Hudson Bay Lynx–Hare population cycles (1845–1935)** using the Lotka-Volterra system of differential equations.

---

## Overview

This project bridges theoretical mathematics and computational data science. The **Lotka-Volterra equations** are a foundational nonlinear ODE system describing the oscillatory dynamics of predator-prey ecosystems. By fitting the model to 90 years of historical Hudson Bay Company fur-trade census data, this project:

1. Validates the theoretical model against real ecological data
2. Demonstrates parameter estimation via numerical optimization
3. Produces interpretable visualizations of population cycles

---

## The Mathematics

The system of two coupled ODEs governing predator-prey dynamics:

$$\frac{dH}{dt} = \alpha H - \beta H L$$

$$\frac{dL}{dt} = \delta H L - \gamma L$$

| Parameter | Ecological Meaning | Optimized Value |
|-----------|-------------------|-----------------|
| $\alpha$ | Hare birth rate | ~0.55 yr⁻¹ |
| $\beta$ | Predation rate | ~0.028 |
| $\delta$ | Lynx growth from predation | ~0.026 |
| $\gamma$ | Lynx death rate | ~0.84 yr⁻¹ |

**Equilibrium point:**
$$H^* = \frac{\gamma}{\delta}, \quad L^* = \frac{\alpha}{\beta}$$

---

## Methodology

1. **ODE Integration** — `scipy.integrate.odeint` for numerical solution
2. **Parameter Optimization** — `scipy.optimize.minimize` with RMSE objective against historical data
3. **Phase Portrait Analysis** — Visualizing the closed-orbit structure around the equilibrium
4. **Stability Analysis** — Linearized Jacobian eigenvalue analysis

---

## Key Results

- Optimized model achieves **strong qualitative agreement** with the observed ~10-year population cycle
- Phase portrait confirms the **neutrally stable centre** predicted by Lotka-Volterra theory
- Quantitative RMSE demonstrates the model's predictive limits due to stochastic ecological factors

---

## Tech Stack

`Python` · `NumPy` · `SciPy` · `Matplotlib`

---

## Repository Structure

```
Lotka-Volterra-Simulation/
├── notebooks/
│   └── 01_lotka_volterra_dynamics.ipynb   # Full analysis notebook
└── README.md
```

---

## Quickstart

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/avinash-chauhan-oss/Lotka-Volterra-Simulation/blob/main/notebooks/01_lotka_volterra_dynamics.ipynb)

---

## Author

**Avinash Chauhan** — BS-MS Mathematics, IISER Thiruvananthapuram  
🌐 [Portfolio](https://avinash-chauhan-oss.github.io)
