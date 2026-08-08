# Predator-Prey Dynamics Analysis 🐇 🐅

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/avinash-chauhan-oss/Lotka-Volterra-Simulation/blob/main/notebooks/01_lotka_volterra_dynamics.ipynb)
![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Library SciPy](https://img.shields.io/badge/Library-SciPy-orange.svg)
![Status Completed](https://img.shields.io/badge/Status-Completed-success.svg)

Mathematical modeling of the Hudson Bay Lynx-Hare population cycles (1845–1935) using Lotka-Volterra differential equations.

## 📌 Project Overview
This project bridges the gap between **Theoretical Mathematics** and **Computational Data Science**. By implementing the Lotka-Volterra system of Ordinary Differential Equations (ODEs), I modeled the famous 10-year ecological cycle of the Hudson Bay Lynx and Snowshoe Hare. 

Using Python and `scipy.integrate.odeint`, I optimized model parameters to accurately fit theoretical predictions to 90 years of historical empirical data.

## 🧠 The Math Behind the Model
The simulation numerically solves the following non-linear system representing predator-prey dynamics:

$$ \frac{dH}{dt} = \alpha H - \beta H L $$

$$ \frac{dL}{dt} = \delta H L - \gamma L $$

| Parameter | Meaning | Value (Optimized) |
| :--- | :--- | :--- |
| $\alpha$ | Hare Birth Rate | `0.55` |
| $\beta$ | Predation Rate | `0.028` |
| $\delta$ | Predator Reproduction | `0.026` |
| $\gamma$ | Predator Mortality | `0.80` |

## 📊 Visualizing the Population Cycles
*Historical Hudson Bay company trading records vs. Numerical ODE Integration.*
![Lotka-Volterra Dynamics](./img/lv_model_fit.png)

## 🚀 Key Results
* **Universal Data Pipeline:** Automated data ingestion from raw GitHub URLs (no local files required).
* **Model Accuracy:** Successfully replicated the ~10-year lag phase between predator and prey population peaks.
* **Sensitivity Analysis:** Demonstrated that a variance in the predation rate ($\beta$) leads to a significant dampening of the population amplitude.

## 🛠️ Tech Stack
* **Core:** Python, NumPy
* **Solver:** `scipy.integrate.odeint`
* **Visualization:** Matplotlib, Pandas

## 💻 How to Run
Click the **"Open in Colab"** badge at the top to run the simulation directly in your browser, or run it locally:

```bash
git clone [https://github.com/avinash-chauhan-oss/Lotka-Volterra-Simulation.git](https://github.com/avinash-chauhan-oss/Lotka-Volterra-Simulation.git)
cd Lotka-Volterra-Simulation
pip install pandas matplotlib scipy jupyter
jupyter notebook notebooks/01_lotka_volterra_dynamics.ipynb
