# Explainability–Governance Score (EGS) Framework

This repository contains the analysis notebooks and supporting implementation used in the study:

**Beyond Predictive Performance: An Explainability–Governance Score Framework for Multidimensional Machine Learning Model Selection**

The study evaluates candidate machine learning models across three high-stakes domains using a multidimensional framework integrating:

- Fidelity
- local predictive Stability
- Counterfactual Actionability
- Governance Alignment

The repository is provided to support transparency, reproducibility, and independent verification of the reported results.

## Repository Structure

EGS-Framework/
- compas/
- cross_domain_and_robustness/
- german_credit/
- pima_diabetes/
- README.md
- requirements.txt

The three domain folders contain the sequential notebooks used for preprocessing, predictive modelling, explainability analysis, counterfactual evaluation, EGS scoring, and results consolidation.

The `cross_domain_and_robustness` folder contains the cross-domain comparison, robustness, sensitivity, statistical evaluation, and publication-output notebooks.

## Data

The study uses three publicly available benchmark datasets:

- German Credit
- Pima Indians Diabetes
- COMPAS

Dataset provenance, analytical sample construction, preprocessing procedures, exclusions, and target definitions are described in the associated manuscript.

Users should obtain the datasets from the public sources described in the manuscript and update local input paths where required.

## Software Environment

The analysis was conducted in Google Colab using:

- Python 3.13.15
- scikit-learn 1.6.1
- XGBoost 3.4.1
- SHAP 0.52.0
- LIME 0.2.0.1
- DiCE 0.12

Additional package dependencies are listed in `requirements.txt`.

## Running the Analysis

Users should clone or download the repository while preserving the relative folder structure.

Within each validation-domain folder, the notebooks are numbered to indicate the intended execution sequence.

The typical workflow is:

1. Exploratory analysis and data inspection
2. Data preprocessing
3. Baseline predictive modelling
4. SHAP analysis
5. LIME analysis
6. SHAP–LIME agreement analysis
7. Counterfactual generation and evaluation
8. EGS preparation and dimension scoring
   - input preparation
   - Fidelity
   - Stability
   - Counterfactual Actionability
   - Governance Alignment
   - composite EGS and weighting analysis
9. Results consolidation

The `cross_domain_and_robustness` folder should be used after the three domain-specific workflows have been completed. It contains analyses for:

- cross-domain framework validation
- alternative weighting sensitivity
- leave-one-dimension-out analysis
- Monte Carlo weight sampling
- repeated full-pipeline robustness analysis
- statistical comparison of candidate models
- consolidated results and publication-ready figures

## File Paths and Outputs

The analysis workflow was developed around the repository folder structure.

Users should preserve the relative directory structure when downloading or cloning the repository. Where local absolute paths are used, these should be updated to the user's own working environment.

Output directories may be changed as required, provided the corresponding paths within the notebooks are updated consistently.

## Reproducibility

The repository contains the implementation used to generate the principal predictive-performance, explainability, EGS, robustness, and statistical results reported in the manuscript.

Fixed model configurations, preprocessing procedures, random seeds, EGS component definitions, and robustness analyses are documented in the manuscript and implemented in the accompanying notebooks.

The EGS is intended as a comparative candidate-model evaluation framework and should be interpreted within the operational definitions, weighting assumptions, and experimental conditions described in the study.
