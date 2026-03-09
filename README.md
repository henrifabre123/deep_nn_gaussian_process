# Empirical Extensions: Gaussian Process Behaviour in Wide Deep Neural Networks

This repository contains the Jupyter Notebook (`Main.ipynb`) used to generate the empirical results for the project report. The code evaluates and extends the theoretical claims made in the paper *Gaussian Process Behaviour in Wide Deep Neural Networks* (Matthews et al., 2018).

## Overview of Experiments

The notebook uses the Maximum Mean Discrepancy (MMD) metric to measure the convergence of finite random neural networks to their Gaussian Process (GP) analogues. It covers the standard prior comparisons and implements four specific extensions:

* **Asymmetric Bottlenecks:** Tests convergence for independent layer growth by comparing symmetric networks ($h_1 = h_2 = n$), slow bottlenecks ($h_1 = \lfloor\sqrt{n/5}\rfloor$, $h_2 = n^2$), and exponential growths ($h_1 = n$, $h_2 = \lfloor e^{n/5}\rfloor$).
* **Convergence Rates:** Quantifies the speed of convergence as a function of the network width scaling parameter $\alpha$, where $h(n) = n^\alpha$.
* **Infinite-Variance Priors:** Demonstrates the failure of the Central Limit Theorem (CLT) when using non-Gaussian weight distributions (Cauchy, symmetric stable, and Student-$t(2)$).
* **Linear Envelope Property (LEP) Violations:** Analyzes the divergence of the network's variance when activation functions strictly violate the LEP condition (testing $u^2$, $u^3$, and $e^{u/4}$).

## Requirements

To run the experiments, the following standard Python packages are required:
* Python 3.x
* NumPy
* Matplotlib (for generating the plots)

## Usage

1. Open `Main.ipynb` in Jupyter Notebook or JupyterLab.
2. Execute the cells sequentially. 
3. The notebook will automatically compute the MMD calculations and generate the corresponding figures used in the final report.
