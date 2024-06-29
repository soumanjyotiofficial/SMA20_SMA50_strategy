This is a sample README file you can use for your trading strategy. It details the trading strategy, the implementation details of the attached script, and the output expected.

---
 Trading Strategy: 20 SMA and 50 SMA

The program establishes a trading strategy based on 20-period and 50-period Simple Moving Averages. The script is supposed to process historical stock data, obtain trading signals according to a given strategy, and plot the equity curve of this strategy. This strategy was an inspiration from various concepts floated in the public domain, almost always through YouTube tutorials.

## Table of Contents
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Usage](#usage)
- [Explanation of the Strategy](#explanation-of-the-strategy)
- [Output](#output)
- [Disclaimer](#disclaimer)

## Introduction

This script will use historical stock data to backtest a trading strategy that involves the 20-period and 50-period SMAs. It generates buy/sell signals, executes trades, and calculates the equity curve to plot the performance of the strategy.

## Requirements

You should have Python installed on your system. You will also have to install the following libraries:

1. pandas
2. numpy
3. matplotlib
4. pandas_ta

All of these packages can be installed from the terminal using the pip package manager. To install pandas, you must use the following command:
```bash
pip install pandas numpy matplotlib pandas_ta
```

## Usage

1. **Prepare your data:**
   - Columns in your data file shall be for `Datetime`, `Open`, `High`, `Low`, `Close`, `Volume`, and `Symbol`.

2. **Run the script:**
   - Save the script given below in a Python file. For example, `trading_strategy.py`.
   - Update the path of the CSV file in the script: `data = pd.read_csv("F:\\JOb Projects\\Python\\NSE_RELIANCE_EQ.csv")`.
   - Run the script:
     ```bash
python trading_strategy.py
     ```

3. **Review the output:**
   - It will print by how many trades the strategy is winning/losing, the accuracy of the strategy and a professional trade history.
   - It will also plot an equity curve.

## Explanation of the Strategy

This program works according to the following rules.
**Signal Generation:**
A buy signal is generated if the price is above both the 20-period and 50-period SMAs, and a 10-minute green candle at 9:20 AM has been observed. On the other side, if the price is less than both the 20-period and 50-period SMAs and a 10-minute red candle is observed at 9:20 AM, then a sell signal will be generated. **Entry and Exit Rules:**
- In the event of a buy signal, break out of the high of the 9:20 AM candle and enter.
- In case of a sell signal, break out of the low of the 9:20 AM candle and enter.
- Set a stop loss and take profit according to a predefined ratio of risk to reward.
At the touch of TP or SL, or at market close, 3:00 PM, the trade is exited.

## Output

The following outputs are obtained from the script whose values are as follows: —
**Trade History**: A record of individual trades, with evidence of entry and exit time and prices and position.
**Win/Loss Statistics**: no. of winning/losing trades, Strategy Accuracy
**Equity Curve**: Plot of Growth in Account Balance from the start

## Disclaimer

This script is strictly for informational and educational purposes. Trading involves risk, and past performance is not indicative of future results. Do your own research on all trading decisions.
