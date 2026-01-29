# Statistical Inference with Incomplete Data

## Overview
This repo contains the analysis and R implementations for an assessment on **Incomplete Data Analysis**, focusing on statistical inference under various missing-data mechanisms and censoring schemes, including theoretical derivations and R simulations.

## Key Topics & Implementations

### 1. Survival Analysis & Type I Censoring
- **Theory:** Derived the PDF and MLEs for **Pareto-distributed** variables under Type I censoring.
- **Inference:** Constructed asymptotic 95% confidence intervals for the shape parameters based on the Fisher Information matrix.

### 2. Multiple Imputation Simulation
- **Goal:** Study the effect that acknowledging/not acknowledging parameter uncertainty when performing multiple imputation might have on the coverage of the corresponding confidence intervals.
- **Target:** Evaluated the empirical coverage probability of confidence intervals for regression coefficients.
- **Method:** Conducted a simulation study ($n=100$ datasets) comparing **Stochastic Regression Imputation** vs **Bootstrap-based Imputation** using the `mice` package.


### 3. Left-Censored Data Analysis
- **Optimisation:** Implemented a custom Log-Likelihood function for **Left-Censored Normal Data** (where values below the threshold $D$ are reported as $D$).
- **Estimation:** Optimised the likelihood function using `optim`/`maxLik` to estimate the mean and variance from a dataset.

### 4. Missing Data Mechanisms (Theory)
- Analysed Bivariate Normal samples to determine **Ignorability** for likelihood-based estimation under different missingness models (MAR vs MNAR) using logistic regression models for the missingness indicator $R$.

### 5. EM Algorithm for Logistic Regression
- **Algorithm:** Derived and implemented a custom **Expectation-Maximisation (EM) Algorithm** from scratch.
- **Application:** Estimated parameters for a Logistic Regression model where the binary response variable has missing values (Bernoulli distribution).

## Tech Stack
- **R Libraries**: `mice` (Multiple Imputation), `maxLik` (Optimisation), `ggplot2`.

## Repo Structure
- `/code`: `.Rmd` files containing the analysis and code.
* `/data`: Datasets (`.Rdata`) used for the simulation and EM algorithm tasks.
* `/docs`: Final report and problem statements.

