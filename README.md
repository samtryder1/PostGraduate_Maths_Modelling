---
title: "Maths Modelling README"
author: "Sam Ryder, 18317496"
date: "`r Sys.Date()`"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# What gives a country better international football tournament-winning odds?


## Basic Overview

This analysis will consider data from multiple sources to build, optimize and test a predictive model to identify the key features in betting odds for the European Football Championships 2024. This analysis is useful to nations looking to build teams who are considered strong contenders to win international tournaments.

## Table of Contents

1. [Installation and Set-Up](#installation-and-set-up)
2. [Data Sources](#data-sources)
3. [Data Collection](#data-collection)
4. [Data Pre-Processing](#data-pre-processing)
5. [Base Modelling](#base-modelling)
6. [Feature Selection](#feature-selection)
7. [Models on Best Features](#models-on-best-features)
8. [Model Optimization](#model-optimization)
9. [Stacking](#stacking)
10. [Feature Importance](#feature-importance)
11. [Feature Importance II] (#feature-importance-II)

## Installation and Set-Up

1. **Python Installation**: This project requires Python. Ensure you have Python installed on your system. You can download Python from the [official Python website](https://www.python.org/downloads/).

2. **Running Jupyter Notebooks**: The Python files for this project are in `.ipynb` format, which can be executed using Jupyter Notebook or Google Colab. To use Jupyter Notebook locally, you can install it via Anaconda or directly using pip:
   - **Using Anaconda**: Install Anaconda from [Anaconda's website](https://www.anaconda.com/products/distribution) and launch Jupyter Notebook from the Anaconda Navigator.
   - **Using pip**: Install Jupyter Notebook with the command:
     ```bash
     pip install notebook
     ```
     


3. **Required Packages**: This analysis requires several Python packages. You can install these packages using pip. The list of packages and their installation commands are provided below. 

      - `pip install beautifulsoup4`
      - `pip install pandas`
      - `pip install numpy`
      - `pip install matplotlib`
      - `pip install scikit-learn`
      - `pip install scipy`
      - `pip install statsmodels`
      - `pip install pygam`
      - `pip install xgboost`
      - `pip install shap`
      - `pip install mlxtend`
      
Once these packages have been installed all import statements should run.


## Data sources
Please note that Fifa Ranking and Odds Data are live data sources so hyperlinks cannot be provided. 

- FIFA Ranking: https://www.sportingnews.com/uk/football/news/fifa-rankings-euro-2024-teams-soccer-uefa-euro-championship/880ff126e23e0e4833ce8e08 
- **[Managerial Data](https://www.transfermarkt.co.uk/europameisterschaft-2024/trainer/pokalwettbewerb/EM24)**
- **[Playing Squad Data](https://www.kaggle.com/datasets/damirdizdarevic/uefa-euro-2024-players)**
- **[Historic Results](https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017?select=results.csv)**
- **[Historic Titles](https://www.uefa.com/uefaeuro/history/winners/)**
- **[Qualifying Record Data](https://footystats.org/international/uefa-euro-qualifiers)**
- Odds Data: https://www.oddschecker.com/football/euro-2024/winner 

## Notebooks
The analysis is performed through several notebooks, each focusing on a specific stage. These notebooks are designed to be run in order with data being defined in earlier notebooks and imported for use in later ones:

![Modelling Process](Modelling_Process.png)
