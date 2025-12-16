# 🌊 1D Simple Harmonic Oscillator (SHO) PINN

This repository contains a **Physics-Informed Neural Network (PINN)** implementation to solve the one-dimensional Simple Harmonic Oscillator (SHO) problem. This project demonstrates how a neural network can be trained to approximate the solution to a Differential Equation (DE) by minimizing the residual of the DE itself, rather than relying solely on large datasets.

## 📁 Project Structure

The core of the project is contained within a single file:

* **`1D Oscillator.ipynb`**: The main Jupyter Notebook. This file includes:
    * **Data Generation:** Creates boundary and initial condition data points.
    * **Model Definition:** Defines the structure of the Neural Network (NN) that will serve as the approximate solution $u(t)$.
    * **Loss Function:** Combines two key loss terms:
        1.  **Data Loss (IC/BC):** Minimizes the error at known initial/boundary conditions.
        2.  **Physics Loss (PDE Residual):** Minimizes the error of the governing equation (the PDE).
    * **Training Loop:** Trains the PINN by minimizing the combined loss function.
    * **Visualization:** Plots the NN's predicted solution against the analytical solution of the SHO.

## 🔬 Physics-Informed Neural Network (PINN)

The Simple Harmonic Oscillator is governed by the second-order ordinary differential equation (ODE):

$$
\frac{d^2u}{dt^2} + \omega^2 u = 0
$$

where:
* $u(t)$ is the displacement of the oscillator as a function of time.
* $\omega$ is the angular frequency.

The PINN works by encoding this equation directly into the loss function. The network is trained to find a function $u_{NN}(t)$ that satisfies both the initial conditions (IC/BC) and minimizes the residual of the ODE across the entire time domain.

## 🛠️ Requirements

To run the Jupyter Notebook locally, you will need:

* Python (3.x)
* JupyterLab or Jupyter Notebook
* The following Python libraries:
    * `torch` (PyTorch) **OR** `tensorflow`
    * `numpy`
    * `matplotlib`
    * `os`
