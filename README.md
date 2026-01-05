# Predator-Prey Dynamics Analysis 🐇🐆

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_COLAB_LINK_HERE)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-SciPy-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)
![License](https://img.shields.io/badge/License-MIT-blue)

> **Mathematical modeling of the Hudson Bay Lynx-Hare population cycles (1845–1935) using Lotka-Volterra differential equations.**

---

## 📌 Project Overview
This project bridges the gap between **Theoretical Mathematics** and **Computational Data Science**. By implementing the **Lotka-Volterra system of Ordinary Differential Equations (ODEs)**, I modeled the famous 10-year ecological cycle of the Hudson Bay Lynx and Snowshoe Hare.

Using **Python** and **SciPy**, I optimized model parameters to fit theoretical predictions to 90 years of historical empirical data.

## 🧠 The Math Behind the Model
The simulation solves the following non-linear system:

$$\frac{dH}{dt} = \alpha H - \beta H L$$
$$\frac{dL}{dt} = \delta H L - \gamma L$$

| Parameter | Meaning | Value (Optimized) |
| :--- | :--- | :--- |
| $\alpha$ | Hare Birth Rate | `0.55` |
| $\beta$ | Predation Rate | `0.028` |
| $\delta$ | Predator Reproduction | `0.026` |
| $\gamma$ | Predator Mortality | `0.80` |

## 🚀 Key Results
* **Universal Data Pipeline:** Automated data ingestion from raw GitHub URLs (no local files required).
* **Model Accuracy:** Successfully replicated the ~10-year lag phase between predator and prey peaks.
* **Sensitivity Analysis:** Demonstrated that a **10% increase in predation rate ($\beta$)** leads to a significant dampening of the population amplitude.

## 🛠️ Tech Stack
* **Core:** `Python`, `NumPy`
* **Solver:** `scipy.integrate.odeint`
* **Visualization:** `Matplotlib`, `Pandas`

## 💻 How to Run
Click the **"Open in Colab"** badge at the top to run the simulation in your browser, or:

```bash
git clone [https://github.com/avinash-chauhan/Predator-Prey-Dynamics.git](https://github.com/avinash-chauhan/Predator-Prey-Dynamics.git)
pip install pandas matplotlib scipy
python Predator_Prey_Dynamics.py
