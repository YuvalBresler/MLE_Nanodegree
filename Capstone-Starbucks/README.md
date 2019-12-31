# Starbucks Capstone Project <!-- omit in toc -->

This is my Capstone Project for Udacity's Machine Learning Engineer Nanodegree.  You can find a Medium article written about this project [here]().

## Table of Contents <!-- omit in toc -->

- [Installation](#installation)
- [Project Overview](#project-overview)
- [File Descriptions](#file-descriptions)
- [Results Summary](#results-summary)

## Installation

To recreate this project you will need:

- Python 3.7.5
- The following Conda and Pip files:

```bash
conda install --file conda_requirements.txt
pip install pip_requirements.txt
```

## Project Overview

Udacity partnered with Starbucks to provide a real-world business problem and simulated data mimicking their customer behavior.  This project is focused on tailoring the personalized offers sent as part of the Starbucks Rewards Program to the customers who are most likely to use them. The Machine Learning terminology for this is "propensity modeling".

We want to determine which kind of offer, if any, to send to each customer based on their purchases and interaction with the previously sent offers. Some customers do not want to receive offers and might be turned off by them, so we want to avoid sending offers to those customers.

## File Descriptions

- **conda_requirements.txt** - The Conda packages required to run this program.
- **data/portfolio.json** - This was provided by Starbucks and contains the information about the offers.  There are a total of 10 offers.
- **data/profile.json** - This was provided by Starbucks and contains demographic information about the customers. There are a total of 17,000 customer profiles.
- **data/transcript.json** - This was provided by Starbucks and contains information about a customer's purchases and their interaction with the offers. There are 306,534 events recorded.
- **pic1.png** - This was provided by Udacity as part of the starter Jupyter Notebook provided by them.
- **pic2.png** - This was provided by Udacity as part of the starter Jupyter Notebook provided by them.
- **pip_requirements.txt** - The Pip packages required to run this program.
- **proposal/proposal.pdf** - My initial proposal for this project.
- **proposal/README.md** - README for my proposal.
- **README.md** - This file.
- **report.pdf** - My final report (the same content as my [Medium article]())
- **Starbucks_Capstone_notebook.ipynb** - My Jupyter Notebook containing all data exploration, cleaning, feature engineering, model building, hyperparameter tuning, and the results.
- **tensorflow_nn.py** - Due to the Jupyter kernel repeatedly crashing when performing hyperparameter tuning with TensorFlow, I wrote the code in a separate file to perform hyperparameter tuning for the neural network.

## Results Summary

The Neural Network model performed the best with an F₂ Score of 0.84863 on the Test Set.

|                  Model                   | Accuracy | F1 Score | F2 Score |  TP   |  FP   |  TN   |  FN   |
| :--------------------------------------: | :------: | :------: | :------: | :---: | :---: | :---: | :---: |
|   Logistic Regression __\[test set\]__   | 0.71208  | 0.79208  | 0.83016  | 4838  | 1737  | 1444  |  803  |
| Support Vector Machines __\[test set\]__ | 0.72463  | 0.78873  | 0.80353  | 4534  | 1391  | 1858  | 1038  |
| Neural Network (Final) __\[test set\]__  | 0.71163  | 0.79726  | 0.84863  | 5002  | 1905  | 1276  |  639  |
