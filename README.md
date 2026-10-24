# ml-implied-volatility-research

# ML-Enhanced Implied Volatility Modelling for Improved Black–Scholes Option Pricing

A machine learning approach to modelling the implied volatility surface and exploring its application to European option pricing.

## Overview

The Black–Scholes model is widely used for pricing European options, but its assumption of constant volatility does not fully capture market phenomena such as volatility smiles and skews.

This research explores a machine learning-enhanced approach that estimates implied volatility from market-related features and integrates the predictions into the Black–Scholes pricing framework. The objective is to investigate whether data-driven volatility estimates can improve pricing accuracy while preserving useful financial interpretations.

## Research Objectives

- Investigate the limitations of constant-volatility assumptions in traditional option pricing.
- Model implied volatility using features such as log-moneyness and time to maturity.
- Compare the performance of multiple regression and ensemble learning approaches.
- Explore the integration of predicted implied volatility into the Black–Scholes pricing framework.
- Examine model performance, volatility surface behaviour, and the limitations of the proposed approach.

## Methodology

The study follows a machine learning pipeline consisting of data preprocessing, exploratory data analysis, feature engineering, model training, hyperparameter tuning, and evaluation.

### Feature Engineering

The primary features include:

- **Log-moneyness:** Represents the relative relationship between the underlying asset price and the option's strike price.
- **Time to maturity:** Represents the remaining time until the option expires.

These features are used to capture variations in implied volatility across strike prices and expiration periods.

### Models Evaluated

The paper compares the following approaches:

- Linear Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost
- Neural Network
- Ensemble model

Hyperparameter tuning using `RandomizedSearchCV` is described for model selection and performance improvement.

### Evaluation

The models are evaluated using Root Mean Squared Error (RMSE) and the coefficient of determination (\(R^2\)). The research also examines the relationship between predicted and market-implied volatility, implied volatility surfaces, option pricing errors, and Delta behaviour.

## Results

The reported model comparison is summarised below.

| Model | RMSE | R² |
|---|---:|---:|
| Linear Regression | 0.238493 | 0.626629 |
| Decision Tree | 0.147263 | 0.857643 |
| Random Forest | 0.134323 | 0.881563 |
| Gradient Boosting | 0.139357 | 0.872519 |
| XGBoost | 0.137151 | 0.876523 |
| Neural Network | 0.136152 | 0.878314 |
| Ensemble | 0.133840 | 0.882410 |

The ensemble achieved the lowest reported RMSE and the highest reported \(R^2\) among the evaluated models.

The paper also investigates the use of machine learning-based volatility estimates within the Black–Scholes framework and reports improvements in option pricing accuracy. These findings should be interpreted in the context of the dataset, experimental setup, and validation methodology described in the manuscript.

## Limitations and Future Work

The study identifies several limitations:

- The approach does not explicitly enforce no-arbitrage constraints.
- Performance depends on the quality, coverage, and distribution of the input data.
- Sparse regions of the volatility surface may result in less reliable predictions.
- The current framework primarily focuses on European-style options.

Potential directions for further research include incorporating arbitrage constraints, exploring temporal models such as LSTMs and transformers, expanding the range of market features, and investigating applications to more complex derivatives.

## Research Paper

The research manuscript is available as a PDF in this repository:

**[ML-Enhanced Implied Volatility Modelling for Improved Black–Scholes Option Pricing](paper.pdf)**

**Status:** Manuscript submitted through the university; publication status pending.

This work is presented as research in progress. The results above reflect those reported in the manuscript.

## Reproducibility

The current repository contains the research manuscript and its documentation. The implementation and experimental environment may be added as they are organised and prepared for release.

The reported metrics should therefore be treated as manuscript-reported results rather than independently reproducible results from this repository.

## Acknowledgements

Research conducted at the School of Computer Engineering, KIIT Deemed to be University.

## Keywords

Machine Learning · Implied Volatility · Black–Scholes · Options Pricing · Random Forest · XGBoost · Ensemble Learning · Quantitative Finance
