# Backtesting Trading Strategies

## Description
This project is a trading strategy that integrates concepts from the [Smart Money Concept Indicator](https://www.luxalgo.com/blog/smart-money-concept-indicator-for-tradingview-free), specifically focusing on bullish and bearish order blocks across three different temporalities. Utilizing the Backtesting.py library, the tool is designed to simulate and optimize trading strategies in historical market conditions, offering insights into the potential viability and profitability of these strategies.

### Key Features:
- Integration of bullish and bearish order blocks from the Smart Money Concept Indicator.
- Multi-temporality analysis to determine aligned trading signals.
- Automatic trade placement when all three temporalities coincide in direction.
- Parameter optimization feature, allowing variation in temporalities, trade direction, swing length, etc.

### Visual Insights

#### Simulated trades example
![Trades of a single run](images/backtest_example.JPG)
*[Complete simulated run of trades with a specific strategy and parameters](backtest_results_sample/SmartMoneyConcepts_2022-04-01-2023-03-31dates_10-10swing_15-60candles.html)*. Upward arrows are long entries, downward arrows are short entries. Green are profitable trades and red are losing trades.

#### Heatmaps
![Heatmap Visualization](images/heatmap.JPG)
*[Heatmap illustrating optimization of specific parameters](backtest_results_sample/parameter_optimization_10_sw.html). The optimal configuration suggests large order blocks. Without trailing stop loss, 3:1 risk ratio, 20% bigger stop loss than the indicator suggests, 48hs order duration. (further testing demonstrated this to be an overfitted example to these specific market conditions)*

#### Order Blocks and Trades
![Order Blocks and Trades](images/candlestick_chart.JPG)
*[Example of traded order blocks](backtest_results_sample/candlestick_stop_limit_3meses.html). Structure is visible as dotted lines indicating ChoCh and BOS. An order block (in this case only buy types are visible) is composed by take profit (green upper bound) and stop loss (red lower bound). Limit price is down the middle.*

## Installation

Follow these steps to set up and run the project:

### Prerequisites

- **Python**: The project is built using Python. If you don't have Python installed, download and install it from [python.org](https://www.python.org/downloads/).

- **CSV with Ticker Data**: You need a CSV file containing ticker data for backtesting. Place this file in the `backtest_data` folder within the project directory.

### Setup

1. **Clone the Repository**: First, clone the repository to your local machine:

   ```
   git clone https://github.com/jmlacasa/backtesting_simulation.git
   cd your-project-name
   ```

2. **Install Required Libraries**: Use the `requirements.txt` file to install the necessary Python libraries. Run the following command:

   ```
   pip install -r requirements.txt
   ```

3. **Prepare the Data**: Ensure you have the CSV file with your ticker data. The file should be placed in the `backtest_data` folder of your project directory. The file should be in the correct format as expected by the scripts.

### Running the Project
After installation, you can run your scripts or modules within the project's directory.

- LuxAlgo for the Smart Money Concept Indicator

## Built With
- [Backtesting.py](https://github.com/kernc/backtesting.py) - Python framework for backtesting trading strategies.
