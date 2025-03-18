# Piecewise Data-Driven Modelling of the RM3 Wave Energy Converter

## Overview
This repository contains the implementation of a piecewise Nonlinear Autoregressive Moving Average with Exogenous Inputs (NARMAX) model to represent the dynamics of the Reference Model 3 (RM3) Wave Energy Converter (WEC). The approach captures system behaviour across different sea states while maintaining computational feasibility.

This work is being submitted to the **2025 European Wave and Tidal Energy Conference (EWTEC)**.

## Dataset
The dataset used in this project is generated through numerical simulations in **WEC-Sim**, a numerical tool for simulating WEC dynamics. The simulations provide:
- **Excitation force** as the system input.
- **PTO (Power Take-Off) position and velocity** as system outputs.
- **Eight different sea states**, each with varying significant wave height (Hs) and peak period (Tp).

The raw data files are stored in CSV format and contain time-series data for each simulated condition.

## Code Structure
The repository includes the following components:

- **`piecewise.ipynb`**: Core script implementing the piecewise NARMAX model.
  - Loads experimental data from CSV files.
  - Applies system identification using NARMAX equations.
  - Generates predictions for PTO position, velocity, and force.
  - Computes performance metrics, such as the root mean squared error (RMSE).
  - Visualises and compares model outputs with real data.

## Dependencies
To run the code, ensure you have the following Python libraries installed:
- `numpy`
- `pandas`
- `matplotlib`

You can install them using:
```bash
pip install numpy pandas matplotlib
```

## Running the Model
To execute the model, simply run the main script:
```bash
python piecewise.ipynb
```
Ensure that the required data files are present in the appropriate directory.

## Contact
For questions or collaboration opportunities, please contact **thalita.nazare.2023@mumail.ie**