# Stock Trader Pro MT5

Stock Trader Pro MT5 is a professional forex trading software developed by Forex Robot Easy Team. This code provides a sample implementation of the trading algorithm used by the Stock Trader Pro MT5 software.

## Product Description
Stock Trader Pro MT5 is a powerful forex trading software designed to help traders make informed trading decisions. It utilizes various technical indicators such as Moving Average, Average True Range, Commodity Channel Index, Stochastic, and Relative Strength Index to identify potential trading opportunities.

The software is designed to open long positions when specific conditions are met, including price being above the Moving Average, Commodity Channel Index being positive, Relative Strength Index being above 50, and Stochastic K being greater than Stochastic D. Additionally, the Stochastic D should be below 20.

Once a long position is opened, the software calculates the lot size based on the account balance and risk. It then sets a Stop Loss and Take Profit based on the input parameters. If the conditions for closing a long position are met, such as price being below the Moving Average, Commodity Channel Index being negative, Relative Strength Index being below 50, or Stochastic K being less than Stochastic D, the software closes the position.

It's important to note that this code provided is a sample implementation and not the official code of the Stock Trader Pro MT5 software. For detailed reviews and trading results of the official product, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/stock-trader-pro-mt5-review-of-a-professional-forex-trading-software/). To find the official developer of this product, please use MQL5.

## Code Explanation
The code begins by defining the necessary input parameters, including Moving Average period, Average True Range period, Commodity Channel Index period, Stochastic K period, Stochastic D period, Relative Strength Index period, Stop Loss in pips, and Take Profit in pips.

The `OnInit()` function is the expert initialization function, where necessary indicators are added using the `IndicatorSetInteger()` and `IndicatorSetString()` functions. In this code, Moving Average, Average True Range, Commodity Channel Index, Stochastic, and Relative Strength Index indicators are added with the specified periods.

The `OnDeinit()` function is the expert deinitialization function, where the added indicators are removed using the `IndicatorRelease()` function.

The `OnTick()` function is the expert tick function, which is called on each tick of the symbol. Inside this function, the current price is obtained using the `SymbolInfoDouble()` function. The values of the indicators are then calculated using the `iMA()`, `iATR()`, `iCCI()`, `iStochastic()`, and `iRSI()` functions.

The code checks if the conditions for opening a long position are met. If the conditions are met, the lot size is calculated based on the account balance and risk. Then, a long position is opened using the `OrderSend()` function. If the position is successfully opened, trade information is printed. If there is an error, the error message is printed.

Next, the code checks if the conditions for closing a long position are met. If a long position is selected using the `OrderSelect()` function, and the conditions for closing a long position are met, the position is closed using the `OrderClose()` function. If the position is successfully closed, trade information is printed. If there is an error, the error message is printed.

Finally, the code includes a section for adding any custom functions required for implementing the trading algorithm.

Please note that this code is a sample implementation and not the official code of the Stock Trader Pro MT5 software.
