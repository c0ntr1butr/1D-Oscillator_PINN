# 1D-Oscillator_PINN
<div>
    <h1>&#x1F30A; 1D Simple Harmonic Oscillator (SHO) PINN</h1>

    <p>
        This repository contains a <strong>Physics-Informed Neural Network (PINN)</strong> implementation to solve the one-dimensional Simple Harmonic Oscillator (SHO) problem. This project demonstrates how a neural network can be trained to approximate the solution to a Differential Equation (DE) by minimizing the residual of the DE itself, rather than relying solely on large datasets.
    </p>

    <h2>&#x1F4C1; Project Structure</h2>

    <p>
        The core of the project is contained within a single file:
    </p>
    <ul>
        <li>
            <strong><code>1D Oscillator.ipynb</code></strong>: The main Jupyter Notebook. This file includes:
            <ul>
                <li><strong>Data Generation:</strong> Creates boundary and initial condition data points.</li>
                <li><strong>Model Definition:</strong> Defines the structure of the Neural Network (NN) that will serve as the approximate solution $u(t)$.</li>
                <li><strong>Loss Function:</strong> Combines two key loss terms:
                    <ol>
                        <li><strong>Data Loss (IC/BC):</strong> Minimizes the error at known initial/boundary conditions.</li>
                        <li><strong>Physics Loss (PDE Residual):</strong> Minimizes the error of the governing equation (the PDE).</li>
                    </ol>
                </li>
                <li><strong>Training Loop:</strong> Trains the PINN by minimizing the combined loss function.</li>
                <li><strong>Visualization:</strong> Plots the NN's predicted solution against the analytical solution of the SHO.</li>
            </ul>
        </li>
    </ul>

    <h2>&#x1F52C; Physics-Informed Neural Network (PINN)</h2>

    <p>
        The Simple Harmonic Oscillator is governed by the second-order ordinary differential equation (ODE):
    </p>
    
    <div style="font-size: 1.2em; text-align: center; margin: 20px 0; padding: 10px; border: 1px solid #ccc; background-color: #f9f9f9;">
        $$
        \frac{d^2u}{dt^2} + \omega^2 u = 0
        $$
    </div>
    
    <p>
        where:
    </p>
    <ul>
        <li>$u(t)$ is the displacement of the oscillator as a function of time.</li>
        <li>$\omega$ is the angular frequency.</li>
    </ul>

    <p>
        The PINN works by encoding this equation directly into the loss function. The network is trained to find a function $u_{NN}(t)$ that satisfies both the initial conditions (IC/BC) and minimizes the residual of the ODE across the entire time domain.
    </p>
    
    

    <h2>&#x1F6E0; Requirements</h2>

    <p>
        To run the Jupyter Notebook locally, you will need:
    </p>
    <ul>
        <li>Python (3.x)</li>
        <li>JupyterLab or Jupyter Notebook</li>
        <li>The following Python libraries:
            <ul>
                <li><code>torch</code> (PyTorch) <strong>OR</strong> <code>tensorflow</code></li>
                <li><code>numpy</code></li>
                <li><code>matplotlib</code></li>
                <li><code>os</code></li>
            </ul>
        </li>
    </ul>
</div>

