# Data-OAMLS

This repository contains the datasets used in the paper:

**OAMLS: Objective-Aware Meta-Learning System for Joint Configuration Selection in Financial Time Series Forecasting**

The datasets are prepared for experiments on financial time series forecasting, volatility-aware asset analysis, cross-asset dependency modeling, and objective-aware meta-learning.

## Overview

The OAMLS framework studies how different forecasting configurations perform across financial assets, market structures, volatility regimes, and forecasting objectives.

In this study, a forecasting configuration is defined as a combination of input representation, forecasting model, loss function, temporal hyperparameters, and market/asset characteristics.

This repository provides the market datasets used to evaluate and reproduce the empirical analysis of the OAMLS study.

## Repository Structure

    Data-OAMLS/
    ├── NASDAQ_stocks.zip
    ├── TSE_stocks.zip
    └── README.md

## Datasets

### NASDAQ Dataset

**File:** `NASDAQ_stocks.zip`

This dataset contains daily historical stock data for **100 large-cap NASDAQ stocks**.

**Time period:** January 2016 – January 2021

The NASDAQ dataset is used to evaluate OAMLS on a developed financial market.

### Tehran Stock Exchange Dataset

**File:** `TSE_stocks.zip`

This dataset contains daily historical stock data for **108 actively traded stocks from the Tehran Stock Exchange (TSE)**.

**Time period:** January 2018 – May 2025

The TSE dataset is used to evaluate OAMLS on an emerging financial market.

## Intended Use

These datasets are intended for academic and research use in:

- Financial time series forecasting
- Stock price movement prediction
- Cross-asset dependency analysis
- Lagged correlation-based feature construction
- Volatility-aware asset clustering
- Objective-aware configuration recommendation
- Meta-learning-based forecasting pipeline selection

The datasets support experiments involving different combinations of:

- Raw closing prices
- Technical indicator-based features
- Lagged correlation-based peer asset features
- Multi-channel input representations
- LSTM, DLinear, and MEAFormer forecasting models
- MSE, Adaptive Loss, and Angle Loss functions

## Role in the OAMLS Framework

The datasets are used in the OAMLS experimental pipeline as follows:

    Raw market data
          ↓
    Preprocessing and normalization
          ↓
    Input representation construction
          ↓
    Volatility-aware asset clustering
          ↓
    Forecasting experiments
          ↓
    Configuration performance logging
          ↓
    Meta-learning dataset construction
          ↓
    Top-K configuration recommendation

## Data Preparation

After cloning this repository, unzip the dataset files:

    unzip NASDAQ_stocks.zip -d NASDAQ_stocks
    unzip TSE_stocks.zip -d TSE_stocks

A recommended structure after extraction is:

    Data-OAMLS/
    ├── NASDAQ_stocks/
    │   └── ...
    ├── TSE_stocks/
    │   └── ...
    ├── NASDAQ_stocks.zip
    ├── TSE_stocks.zip
    └── README.md

## Example Usage

These datasets can be used together with the OAMLS source code repository.

A typical workflow is:

    git clone https://github.com/alihaghighat/Data-OAMLS.git
    cd Data-OAMLS

    unzip NASDAQ_stocks.zip -d NASDAQ_stocks
    unzip TSE_stocks.zip -d TSE_stocks

Then, set the extracted dataset paths in the OAMLS code repository configuration files.

Example:

    data:
      nasdaq_path: "../Data-OAMLS/NASDAQ_stocks"
      tse_path: "../Data-OAMLS/TSE_stocks"

## Citation

If you use this dataset repository, please cite the associated paper:

    @article{haghighat_oamls,
      title   = {OAMLS: Objective-Aware Meta-Learning System for Joint Configuration Selection in Financial Time Series Forecasting},
      author  = {Haghighat, Ali and Moosavi, Mohammad R.},
      journal = {Expert Systems with Applications},
      year    = {2026},
      note    = {Manuscript under review}
    }

## Related Repository

The source code for the OAMLS framework will be provided separately.

Recommended repository names:

- `OAMLS`
- `OAMLS-Code`

## Data Availability

The datasets are provided to support reproducibility of the OAMLS experiments.

The NASDAQ dataset contains historical market data from publicly available financial sources.

The TSE dataset contains historical daily stock data collected from publicly available Tehran Stock Exchange sources.

## License

Please check the license file before using this repository.

If no license is provided, the datasets should be considered available for academic and non-commercial research use only until a formal license is added.

## Contact

For questions regarding the dataset or the OAMLS paper, please contact:

**Ali Haghighat**  
Shiraz University  
Email: haqiqat@shirazu.ac.ir

**Mohammad R. Moosavi**  
Shiraz University  
Email: smmosavi@shirazu.ac.ir
