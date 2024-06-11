# TA, find optimal parameters for each asset

This trading strategy is designed for the [Quantiacs](https://quantiacs.com/contest) platform, which hosts competitions
for trading algorithms. Detailed information about the competitions is available on
the [official Quantiacs website](https://quantiacs.com/contest).

## How to Run the Strategy

### In an Online Environment

The strategy can be executed in an online environment using Jupiter or JupiterLab on
the [Quantiacs personal dashboard](https://quantiacs.com/personalpage/homepage). To do this, clone the template in your
personal account.

### In a Local Environment

To run the strategy locally, you need to install the [Quantiacs Toolbox](https://github.com/quantiacs/toolbox).

## Overview

This notebook provides a comprehensive guide to finding optimal parameters for technical analysis strategies for various
assets. It emphasizes reducing the risk of overfitting by using multiple parameter sets for each asset. The notebook is
structured as follows:

### Sections:

1. **Introduction and Strategy Explanation**:
    - Discusses the importance of adjusting technical indicators' parameters for each asset.
    - Highlights the risk of overfitting and suggests using multiple parameter sets to mitigate it.

2. **Base Strategy Implementation**:
    - Implements a basic trend-based strategy using a moving average (MA) indicator.
    - The `strategy_long` function defines the strategy, calculating buy and stop signals based on the rate of change (
      ROC) of the MA.

3. **Performance Evaluation**:
    - Evaluates the performance of the base strategy.
    - Uses statistical and graphical tools to assess the strategy's results.

4. **Optimization for All Assets**:
    - Demonstrates optimization of the strategy for all assets simultaneously.
    - Uses the `optimize_strategy` function to find the best MA period that maximizes the Sharpe ratio.
    - Visualizes the optimization results.

5. **Optimization for Each Asset**:
    - Conducts a detailed optimization for each asset individually.
    - Shows how to scan through a range of parameters to find the best ones for each asset.
    - Interactive visualization of optimization results for individual assets.

6. **Selection of Best Parameters**:
    - Provides methods to select the best parameters for a fixed number of assets.
    - Selects multiple sets of parameters to reduce the risk of overfitting.
    - Saves the selected configuration to a JSON file.

7. **Final Strategy Implementation**:
    - Combines the individual asset optimizations into a final strategy.
    - The `optmized_strategy` function aggregates results from different parameter sets to form the final strategy.

8. **Final Performance Evaluation**:
    - Evaluates the performance of the optimized strategy.
    - Outputs key performance statistics and major plots.

9. **Best Practices and Tips**:
    - Recommends splitting data into training and testing sets to detect overfitting.
    - Suggests running the optimizer on all available data before final submission.

### Key Points:

- **Technical Analysis**: The notebook leverages technical indicators, specifically the moving average, to build trading
  strategies.
- **Optimization**: Emphasizes the importance of optimizing parameters for each asset and suggests methods to mitigate
  overfitting.
- **Performance Evaluation**: Uses comprehensive statistical and graphical analysis to evaluate strategies.
- **Final Strategy**: Combines multiple optimized parameter sets to create a robust final trading strategy.

This notebook is a valuable resource for quantitative researchers and algorithmic traders aiming to optimize and
evaluate technical analysis-based trading strategies across multiple assets.
