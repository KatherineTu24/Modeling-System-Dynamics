# MSD Group Project - Malaria System Dynamics Model

This project contains a system dynamics model for analyzing malaria transmission, economic impacts, and intervention policies.

## Model Files

### `balariainbali-Policies.mdl`
Main Vensim system dynamics model implementing a comprehensive malaria transmission model with policy interventions. Includes:
- Human and mosquito population dynamics (susceptible, infected, recovered/exposed states)
- Economic feedback loops (GDP per capita, healthcare quality, economic losses)
- Policy interventions: bed nets, vaccines, and larval control
- Simulation runs for 2000 months with configurable parameters

### `CLD.mdl`
Basic causal loop diagram (CLD) model showing fundamental relationships between:
- GDP per capita and economic growth
- Healthcare quality and recovery rates
- Mosquito population dynamics
- Human infection and recovery processes

### `CLD_policies.mdl`
Extended CLD model incorporating policy interventions:
- Prevention funding allocation
- Bed net coverage and bite protection
- Vaccine coverage and effective immunity
- Policy impact on transmission dynamics

## Analysis Notebooks

### `OptimizationAndCalibration.ipynb`
- **Optimization**: Finds parameter values that minimize disease burden (total infections)
- **Calibration**: Fits model parameters to match real-world data using least squares optimization
- Uses differential evolution and L-BFGS-B optimization algorithms

### `PoliciySimulation.ipynb`
Policy intervention analysis and optimization:
- Simulates bed net and vaccine interventions
- Optimizes GDP allocation for prevention (0.5-5%) and resource allocation between nets and vaccines
- Compares theoretical baseline vs. calibrated parameter sets
- Outputs optimal coverage strategies

### `stochasticity.ipynb`
Stochastic analysis examining:
- Non-linear system behavior and tipping points
- Impact of parameter uncertainty on model outputs
- Noise amplification through system dynamics
- Uses Monte Carlo simulations with parameter variation

## Data Files

### `gdp-per-capita-worldbank.csv`
GDP per capita (PPP, constant 2021 international $) data for Mali from 1990-2023, sourced from World Bank via Our World in Data.

### `incidence-of-malaria.csv`
Malaria incidence rates (per 1,000 population at risk) for Mali from 2000-2020, used for model calibration.

### `population-growth-rates.csv`
Historical population growth rate data for Mali from 1950 onwards, used for demographic modeling.

## Dependencies

- Python: `numpy`, `pandas`, `scipy`, `matplotlib`
- System Dynamics: `pysd` (for Vensim model integration)
- Vensim DSS/PLE (for `.mdl` file editing)

## Usage

1. **Model Simulation**: Open `.mdl` files in Vensim or use `pysd` in Python
2. **Analysis**: Run Jupyter notebooks for optimization, calibration, and policy analysis
3. **Data Integration**: CSV files can be imported for calibration and validation

