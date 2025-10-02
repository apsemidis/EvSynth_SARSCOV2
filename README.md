# Bayesian Evidence Synthesis for Modeling SARS-CoV-2 Transmission

This repository contains the code accompanying the paper:

**Anastasios Apsemidis and Nikolaos Demiris**  
*Bayesian evidence synthesis for modeling SARS-CoV-2 transmission*  
Journal of the Royal Statistical Society Series A: Statistics in Society, (in press).  
DOI: *to be added*

---

## Abstract
The acute phase of the Covid-19 pandemic has made apparent the need for decision support based upon accurate epidemic modeling. This process is substantially hampered by under-reporting of cases and related data incompleteness issues. In this article we adopt the Bayesian paradigm and synthesize publicly available data via a discrete-time stochastic epidemic modeling framework. The models allow for estimating the total number of infections while accounting for the endemic phase of the pandemic. We assess the prediction of the infection rate utilizing mobility information, notably the principal components of the mobility data. We evaluate variational Bayes in this context and find that Hamiltonian Monte Carlo offers a robust inference alternative for such models. We elaborate upon vector analysis of the epidemic dynamics, thus enriching the traditional tools used for decision making. In particular, we show how certain 2-dimensional plots on the phase plane may yield intuitive information regarding the speed and the type of transmission dynamics. We investigate the potential of a two-stage analysis as a consequence of cutting feedback, for inference on certain functionals of the model parameters. Finally, we show that a point mass on critical parameters is overly restrictive and investigate informative priors as a suitable alternative.

---

## Repository structure
- `[R] SEIR_vacc_dem_model.txt` – R code for the SEIR vaccination-demography model for Greece  
- `[R] Mobility_analysis.txt` – R code for mobility data analysis and prediction of infection rates  
- `STAN_models.txt` – Collection of Stan models (SIR/SEIR variants with vaccination and demography components)  

---

## Requirements
- **R** ≥ 4.0  
- R packages:  
  - `rstan`, `bridgesampling`, `loo`, `ggplot2`, `bayesplot`, `mgcv`, `xgboost`  
- Data files (not included here):  
  - `confirmed.txt` (daily confirmed cases by country)  
  - `deaths.txt` (daily deaths by country)  
  - `vaccinations_gr.txt` (vaccination data for Greece)  
  - `mobility_google.csv` and `mobility_apple.csv` (mobility data sources)

Due to licensing restrictions, raw data are not included in this repository. Please download from official sources (e.g., Johns Hopkins CSSE, Our World in Data, Google/Apple mobility).

---

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/apsemidis/EvSynth_SARSCOV2.git
   cd EvSynth_SARSCOV2
   ```

2. Prepare input data:  
   Place `confirmed.txt`, `deaths.txt`, `vaccinations_gr.txt`, `mobility_google.csv`, `mobility_apple.csv` in the working directory.

3. Run the SEIR model:
   ```R
   source("[R] SEIR_vacc_dem_model.txt")
   ```

4. Run the mobility analysis:
   ```R
   source("[R] Mobility_analysis.txt")
   ```

---

## Citation
If you use this code, please cite:  

> Apsemidis, A. and Demiris, N. *Bayesian evidence synthesis for modeling SARS-CoV-2 transmission.* Journal of the Royal Statistical Society Series A, (in press). DOI: *to be added*.

---

## Contact
- Anastasios Apsemidis – [apsemidis@aueb.gr](mailto:apsemidis@aueb.gr)  
- Nikolaos Demiris – [nikos@aueb.gr](mailto:nikos@aueb.gr)  
