# Supervised Learning
## Capstone Project: Walmart Store Sales Forecast

## Project Overview
Walmart is an American multinational retail corporation that operates a chain of hypermarkets, department stores and grocery stores. As of Jul 2019, Walmart has 11,200 stores in 27 countries with revenues exceeding $500 billion. A challenge facing the retail industry such as Walmart’s is to ensure the supply chain and warehouse space usage is optimized to ensure supply meets demand effectively, especially during spikes such as the holiday seasons. 
This is where accurate sales forecasting enable companies to make informed business decisions. Companies can base their forecasts on past sales data, industry-wide comparisons and economic trends. However, a forecasting challenge is the need to make decisions based on limited history. If Christmas comes but once a year, so does the chance to see how strategic decisions impacted the bottom line. 

## Problem Statement
Historical sales data for 45 Walmart stores located in different regions has been provided. Each store contains many departments, and the sales for each department in each store needs to be projected. Additionally, Walmart runs several promotional markdown events throughout the year. These markdowns precede prominent holidays, the four largest of which are the Super Bowl, Labor Day, Thanksgiving, and Christmas. The weeks including these holidays are weighted five times higher in the evaluation than non-holiday weeks. These markdowns are known to affect sales, but it is challenging to predict which departments are affected and the extent of the impact.

This problem is sourced from Walmart's [Kaggle Competition](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/overview).


### Install

This project requires **Python 3.x** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [XGBoost](https://xgboost.readthedocs.io/)
- [LightGBM](https://lightgbm.readthedocs.io/en/latest/)

You will also need to have software installed to run and execute an [iPython Notebook](http://ipython.org/notebook.html)

### Code

This project contains four files:

- `WalmartStoreSales.ipynb`: This is the main Jupyter Notebook with the project code.
- `stores.csv`: The stores dataset. Will be processed by the notebook.
- `features.csv`: The features dataset. Will be processed by the notebook.
- `train.csv`: The training dataset. Will be processed by the notebook.
- `test.csv`: The testing dataset. Will be processed by the notebook.


### Run

In a terminal or command window, navigate to the top-level project directory `finding_donors/` (that contains this README) and run one of the following commands:

```bash
ipython notebook WalmartStoreSales.ipynb
```  
or
```bash
jupyter notebook WalmartStoreSales.ipynb
```

This will open the iPython Notebook software and project file in your browser.

### Data
The dataset for this project is provided by Walmart on [Kaggle](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/data) and contains 4 files. 

1. **stores.csv**: Contains anonymized information about the 45 stores, indicating the type and size of store.
   - `Row Count: 45`
   - `File Size: 1 KB`

2. **features.csv**: Contains additional data related to the store, department, and regional activity for the given dates. 
   - `Row Count: 8191`
   - `File Size: 579 KB`

3. **train.csv**: This is the historical training data, which covers to 2010-02-05 to 2012-11-01
   - `Row Count: 422000`
   - `File Size: 12542 KB`

4. **test.csv**: Identical to train.csv, except weekly sales data is withheld. 
   - `Row Count: 115000`
   - `File Size: 2538 KB`

**Features**
- `Store`: Store Number
- `Type`: Store Type (A, B & C)
- `Size`: Store Size
- `Date`: The Week (YYYY-MM-DD)
- `Temperature`: Average Temperature
- `Fuel_Price`: Cost of Fuel
- `MarkDown1`: Promotional Markdown #1
- `MarkDown2`: Promotional Markdown #2
- `MarkDown3`: Promotional Markdown #3
- `MarkDown4`: Promotional Markdown #4
- `MarkDown5`: Promotional Markdown $5
- `CPI`: Consumer Price Index
- `Unemployment`: Unemployment Rate
- `IsHoliday`: Is Holiday Week (Y or N)
- `Dept`: Department Number

**Target Variable**
- `Weekly_Sales`: Weekly Sales

### Appendix
My solution to the problem is also available as a [Kaggle Kernel](https://www.kaggle.com/nitinx/storesales-randomforest-light-gbm-stacking)