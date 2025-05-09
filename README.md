# Stock Market Dashboard
## Overview
This project involves the creation of an interactive stock market dashboard using Tableau, where data is manipulated and processed using Python’s Pandas library. The dashboard showcases key stock performance metrics like the 50-day and 200-day moving averages, percentage changes in stock prices, and volume variations, allowing users to make data-driven comparisons for stock analysis.

## Data Source
The dataset used for this project is the Stock Market Dataset, which includes historical stock prices and volumes for various companies.

## Data Processing
Using Python and Pandas, the following key metrics were computed:

50-Day Moving Average (MA50): A common technical indicator used to smooth out price data over a specified time period.

200-Day Moving Average (MA200): Another important moving average used to track long-term trends.

Percentage Change in Price: Measures the rate of change in stock prices over time.

Percentage Change in Volume: Tracks the percentage change in trading volumes, helping to identify unusual trading activity.

These columns were calculated and used to enhance the stock analysis capabilities of the Tableau dashboard.

## Features of the Dashboard
Interactive Data Visualization: Allows users to explore stock performance visually.

Real-time Comparison: Compare key stock metrics such as the moving averages, price changes, and volume fluctuations across different companies and time periods.

## Getting Started
Download the dataset from this link.

Load the data into your Python environment.

Use Pandas to calculate the desired metrics (MA50, MA200, percent changes).

Import the processed data into Tableau to create the interactive dashboard.

## Prerequisites
Python 3.x

Pandas

Tableau (for data visualization)

## Example Code
import pandas as pd

### Load the dataset
data = pd.read_csv('stock_data.csv')

### Calculate Moving Averages
data['MA50'] = data['Close'].rolling(window=50).mean()
data['MA200'] = data['Close'].rolling(window=200).mean()

### Calculate Percent Change in Price and Volume
data['Price_Change'] = data['Close'].pct_change() * 100
data['Volume_Change'] = data['Volume'].pct_change() * 100
