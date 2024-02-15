# Average Levels

This code is an Expert Advisor (EA) for the MetaTrader 5 platform. It calculates the average entry level, stop loss level, and take profit level for all trades on a given symbol. It also draws these average levels on the chart.

## Usage

To use this code, follow these steps:

1. Open the MetaTrader 5 platform.
2. Compile and run the code as an Expert Advisor.
3. Set the input parameters according to your preferences.
4. The code will calculate the average levels and draw them on the chart.

## Input Parameters

The code has the following input parameters:

- SeparateLevels (bool): Option to calculate average levels separately for Buy and Sell trades.
- LevelColor (color): Color of the level lines.
- LabelColor (color): Color of the level price labels.
- LevelStyle (int): Style of the level lines.
- LabelFontSize (int): Font size of the level price labels.

## How It Works

1. The code initializes by calling the `OnInit` function. This function calculates the average levels for all trades on the given symbol using the `CalculateAverageLevels` function.
2. The code then enters the main loop and calls the `OnTick` function on each tick. However, in this code, the `OnTick` function does nothing.
3. The `CalculateAverageLevels` function iterates through all trades using the `OrdersTotal` and `OrderSelect` functions.
4. For each trade, it checks if the trade symbol matches the given symbol.
5. If the symbols match, it calculates the average levels by summing the open price, stop loss, and take profit levels multiplied by the lot size.
6. It also keeps track of the total lot size.
7. After iterating through all trades, it divides the sum of the levels by the total lot size to get the average values.
8. Finally, it calls the `DrawLevel` function to draw the average levels on the chart.

## Product Description

Average Levels is a powerful tool for optimizing trade entries and exits in the Forex market. It calculates the average entry level, stop loss level, and take profit level for all trades on a specific symbol. These average levels provide valuable insights into the market dynamics and can be used to fine-tune trading strategies.

Key Features:
- Calculate average entry, stop loss, and take profit levels for all trades on a given symbol.
- Option to calculate average levels separately for Buy and Sell trades.
- Customizable level color, label color, level style, and label font size.
- Drawn levels can be easily removed from the chart.

Average Levels is designed to assist traders in making informed trading decisions by providing a clear visualization of the average levels based on historical trade data. By analyzing these levels, traders can identify potential entry and exit points, optimize their trading strategies, and improve overall trading performance.

Please note that ForexRobotEasy is not the official developer of this product. We provide this sample code to demonstrate how the product works. To find the official developer of this product and access detailed reviews and trading results, please visit [this link](https://forexroboteasy.com/forex-robot-review/review-average-levels-forex-software-optimize-trade-entries-exits/).

For more information and to download the official version of this product, please visit the MQL5 website.
