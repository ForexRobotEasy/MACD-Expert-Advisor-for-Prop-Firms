# MACD Expert Advisor for Prop Firms

This is a sample code for a MACD (Moving Average Convergence Divergence) Expert Advisor designed for Prop Firms. This code is provided by ForexRobotEasy Team and is not the official developer of this product. To find the official developer of this product, please use MQL5.

## Product Description

This MACD Expert Advisor is designed for Prop Firms and aims to generate trading signals based on the MACD indicator. The Expert Advisor opens trades when the MACD histogram changes from negative to positive or vice versa.

Key Features:
- Trade lot size: configurable with input parameter `Lots`.
- Stop loss: configurable with input parameter `StopLoss` (in pips).
- Take profit: configurable with input parameter `TakeProfit` (in pips).
- MACD indicator settings: fast EMA period = 12, slow EMA period = 26, signal SMA period = 9.

## How it Works

1. The Expert Advisor includes the necessary libraries `Trade.mqh` and `MovingAverages.mqh`.
2. Input parameters are defined, including `Lots` (trading lot size), `StopLoss` (stop loss in pips), and `TakeProfit` (take profit in pips).
3. Global variables are initialized, including `CTrade` object `trade` for executing trades and `CMovingAverage` object `MA` for calculating moving averages.
4. The `OnInit` function is called during Expert Advisor initialization. It sets up the MACD indicator, calculates MACD values, and stores them in arrays `macdMain`, `macdSignal`, and `macdHist`.
5. The `OnTick` function is called on each tick of the chart. It checks for trading signals based on the MACD histogram values.
   - If the current MACD histogram value (`macdHist[0]`) is greater than 0 and the previous value (`macdHist[1]`) is less than 0, a buy trade is opened using the `trade.Buy` function.
   - If the current MACD histogram value is less than 0 and the previous value is greater than 0, a sell trade is opened using the `trade.Sell` function.
6. The `OnDeinit` function is called when the Expert Advisor is removed from the chart. It closes any open trades using the `trade.PositionCloseAll` function.

## Product Review and Trading Results

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/macd-expert-advisor-unbiased-review-for-prop-firms/). Please note that ForexRobotEasy is not the official developer of this product. This code is provided as a sample that can work as described in the product.

For official developer information, please use MQL5.
