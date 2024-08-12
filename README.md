# IDL-Stock-Predictive-Model

## Overview

Stock market prediction remains a complex challenge due to the intrinsic volatility and myriad factors influencing stock prices. Traditional machine learning models, while foundational, often fall short when applied to real-time data, particularly in predicting short-term market movements. Recent advances have seen the integration of CNN and LSTM networks, which capture both spatial features and temporal patterns in stock data effectively.

## Intended Audience

This project is specifically designed for our team's internal use and development. It is part of our ongoing efforts to enhance our predictive capabilities in the stock market domain.

## Directory Structure

```
root
│
└───Data
│   │   .DS_Store
│   │   data.csv
│   │   data2.csv
│   │   AAPL.csv
│   │   AAPL_sorted
│   │   aapl_financial_news_avg_2020-now.csv
│   │   aapl_intraday_historical_stock_market_2020-now.csv
│   │   combined_data_sentiment.csv

└───.DS_Store
└───IDL_Project_MidTerm.ipynb
└───IDL_Project_S24_v1_0-2.ipynb
└───README.md
```

- Data/                          -> Contains the datasets used for model training and testing.
- .DS_Store                      -> System file for macOS folder properties (not relevant to the project's functionality).
- IDL_Project_MidTerm.ipynb      -> Jupyter notebook containing exploratory data analysis and preliminary findings for the midterm.
- IDL_Project_S24_v1_0-2.ipynb   -> Main Jupyter notebook for the stock prediction model. This notebook includes data preprocessing, model training, and evaluation.
- README.md                      -> Documentation for using and understanding the project.
             

## Installation

Please follow the installation steps provided within the idl_project_s24_v1_0-2.ipynb file. This section includes all necessary libraries and dependencies you need to install before running the project. Run the cell for "Installs" and "Imports" sections.

## Code Structure

The code is divided into several sections there are:

- Installs: Check nvidia-smi, and run several necessary libraries such as wandb, seaborn, etc.
- Imports: Imports all necessary packages for the project.
- Configuration: Configuration in a YAML file that will be injected in the program thread on the go.
- Dataset: Loading the dataset from the CSV file and plots for graphical representation and verification. Also includes the DataLoader in which we implement normalization. Note that this section has old data and new data since the new data is the dataset that we created as a novelty for this project.
- Model Architecture: It contains code for Transforer Utilities, CNN-LSTM Encoder, Transformer Encoder, and Transformer Decoder.
- Stock Predictor Architecture: This is the class wrapper that is used for entire model instance.
- Model Setup: It creates an instance of the model.
- Model Summary: Helper function for printing model summary for more flexibility. 
- Test Model: Test the instance created previosuly. 
- Loss, Optimizer, Scheduler, Scaler: Create instances for loss function, optimizer, and scheduler. 
- WandDB: Login to WanDB account for logging your run.
- Training, Validation Modules: Training and validation methods.
- Experiments: Run experiements.
- Old Test: Run the predictions test

## Dataset

There are multiple dataset files that you can play with. The baseline dataset that we used is the _data.csv_ and _data2.csv_.

The RAW Apple Inc (AAPL) stock that we used is within _AAPL.csv_ file. We use this dataset to clean it, normalize it, and sort it in ascending order. The resulting data is in _AAPL_sorted.csv_, which we used for our experiments without sentiment scores.

The Final data that we used with added sentiment analysis is the _combined_data_sentiment.csv_.

## Usage

The codebase was initially developed in a Python Notebook, making it modular and easy to run in segments. You can execute the code by running combinations of cells that represent different sections of the process. For example, run the following cells to test sentiment dataset on CNN-LSTM Encoder + Transformer Decoder Architecture:

1. Installs
2. Imports
3. Configuration
4. Sentiment Data
5. Utilities
6. CNN-LSTM Encoder
7. Transformer Decoder
8. Stock Predictor Architecture
9. Model Setup
10. Model Summary
11. Loss, Optimizer, Scheduler, Scaler
12. WanDB
13. Training, Validation Modules
14. Training and Validation under Experiments
15. Testing

Please refer to the comments within each cell for guidance on how to proceed with running the sections.

## Technologies

This project utilizes Python along with several deep learning libraries like PyTorch which are detailed in the installation section of the code. There is no additional technology or external dependency required.

## No Licensing Information

This project does not currently include any specific licensing information or contribution guidelines.
