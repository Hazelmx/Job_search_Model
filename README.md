# Job_search_Model
This repository contains a simulation-based study of the McCall job-search model, extended with reinforcement learning (Q-learning) and Bayesian updating for unknown wage-offer distributions. The project compares classical dynamic programming methods with machine learning approaches to study convergence, reservation wages, and unemployment dynamics.
This project also links a Python implementation of the job search model with a NetLogo agent-based simulation.

## Theratical foundation

job_search_model.pdf provides the theoretical foundation and mathematical derivation of the McCall job-search model.

It explains how unemployed workers decide whether to accept or reject wage offers by solving dynamic programming problems. 

The document derives the Bellman equation, introduces the concept of the reservation wage, and extends the framework to cases with unknown wage distributions.

It also formalizes Bayesian belief updating and develops the Reservation Wage Fixed-Point Equation (RWFE), which links beliefs about wage distributions to optimal job acceptance thresholds.

 ## Python code Contents

Job Search Model (Search with Learning).ipynb
Main Jupyter notebook containing:

### 1. Model setup and parameterization

Method 1 – Value Function Iteration (VFI): Solves the Bellman equation to compute optimal reservation policies.

Method 2 – Reservation Wage Functional Equation (RWFE): Faster fixed-point iteration approach using operator mappings.

Offer Distribution Unknown Model: Extends the baseline by incorporating Bayesian belief updating over competing wage distributions.

Q-learning Implementation: Uses temporal-difference learning with an ε-greedy policy, Monte Carlo draws, and vectorized simulation.

Simulations & Plots: Demonstrates unemployment dynamics under different wage-offer distributions and learning setups.

### 2. Methods Implemented

**Dynamic Programming Baseline:** 
1.Bellman equation solved by VFI. 

2.Visualizes convergence of value functions and reservation wages.

**Q-learning with Temporal-Difference Updates:**

1.Implements an agent-based simulation with exploration–exploitation tradeoffs. 

2.Compares learning outcomes against the dynamic-programming baseline.

**Unknown Wage-Offer Distributions:** 

1.Bayesian learning over Beta families of wage distributions. 

2.Reservation Wage Functional Equation (RWFE) solved via operator iteration and bilinear interpolation.


## NetLogo code Contents

Reservation function imported: NetLogo loads reservation_wage.csv.

Regime-change button: switch true distribution from g to f.

Plots included: Unemployment rate, Average belief, Average reservation wage, Belief distribution histogram

## Workflow

### 1.Run Python solver: Solving the Reservation Wage Function

** File: Job Search Model (Search with Learning).ipynb **

The Python code uses NumPy and Numba to:

Define wage offer distributions f and g (Beta distributions).

Compute the reservation wage function (w̄(π)) as a fixed point of the Bellman operator.
Save the solution as a CSV file for NetLogo.

** This generates reservation_wage.csv. **

### 2. Open NetLogo model:  Heterogeneous Agent Simulation

** File: job-search-model1.nlogo **

Ensure reservation_wage.csv is in the same directory.

Click setup, then go.

### 3. Experiment

Adjust sliders for number of workers.

Click regime-change at a chosen tick to simulate a shock.

Watch how unemployment, beliefs, and reservation wages evolve.
