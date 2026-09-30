# Reproduction: Levy SEIR Model for Epidemiological Modeling

## 📌 Overview
This repository contains my from-scratch implementation and reproduction of the Levy SEIR model. The goal is to understand how Levy processes (stochastic jumps) affect the spread of infectious diseases compared to the standard deterministic SEIR model.

## 🧮 Model Equations (Deterministic SEIR with Media Coverage)

The model divides the population into four compartments:
- **S(t):** Susceptible
- **E(t):** Exposed
- **I(t):** Infectious
- **R(t):** Recovered

The deterministic system of ordinary differential equations (ODEs) is:

$$
\begin{aligned}
\frac{dS}{dt} &= A - \left(\beta_1 - \frac{\beta_2 I}{\alpha + I}\right) \frac{SI}{N} - \mu S \\
\frac{dE}{dt} &= \left(\beta_1 - \frac{\beta_2 I}{\alpha + I}\right) \frac{SI}{N} - (k + \mu)E \\
\frac{dI}{dt} &= kE - (m + \mu)I \\
\frac{dR}{dt} &= mI - \mu R
\end{aligned}
$$

### 📖 Explanation of Every Symbol:
- **S, E, I, R:** Susceptible, Exposed, Infectious, Recovered populations.
- **N:** Total population (\(N = S + E + I + R\)).
- **A:** Recruitment rate (births/immigration into the susceptible pool).
- **β₁:** Baseline transmission rate.
- **β₂:** Media coverage factor (reduces transmission as infections rise).
- **α:** Media coverage saturation constant.
- **μ:** Natural death rate (for all compartments).
- **k:** Rate at which exposed individuals become infectious (incubation rate).
- **m:** Recovery rate of infectious individuals.

## 📄 Original Paper
- **Paper Title:** Stochastic analysis of COVID-19 by a SEIR model with Lévy noise
- **Authors:** Yamin Ding, Yuxuan Fu, Yanmei Kang
- **Link:** https://doi.org/10.1063/5.0003705

## 🎯 Objectives
- [ ] Implement the standard deterministic SEIR model.
- [ ] Implement the Levy process (stochastic noise/jumps).
- [ ] Compare the results (deterministic vs. stochastic).
- [ ] Write a technical report documenting the reproduction.

## 🛠️ Tools Used
- Python
- NumPy / SciPy
- Matplotlib
- Jupyter Notebook

## 📂 Repository Structure
- `data/` : Data files (if any)
- `notebooks/` : Jupyter notebooks for experiments
- `src/` : Python source code
- `results/` : Plots and output figures

## 🚀 Status
- [x] Repository initialized
- [ ] Phase 1: Foundation
- [ ] Phase 2: Basic SEIR Implementation
- [ ] Phase 3: Levy Process Integration
- [ ] Phase 4: Analysis & Documentation

## 👤 Author
**Mamunur Rashid**
- GitHub: [@mamunur-cou](https://github.com/mamunur-cou)
- LinkedIn: [Mamunur Rashid](https://www.linkedin.com/in/mamunur-rashid-cou/)
