# Polymarket Arbitrage Analysis

## Overview
This project acts as a quantitative development framework to analyze statistical arbitrage opportunities between Polymarket (prediction market) and Spot Markets (Binance/Coinbase). It specifically tests the hypothesis of whether Polymarket's implied price leads the Spot market price.

## Mathematical Framework

### 1. Implied Expected Value ($P_{implied}$)
We define the implied expected value of the asset based on the binary option price on Polymarket:

$$ P_{implied} = P_{Poly} \times K $$

Where:
- $P_{Poly}$: The probability (price) of the "Yes" outcome on Polymarket (0 to 1).
- $K$: The Strike Price of the contract.

### 2. Arbitrage Deviation ($D$)
$$ D = P_{Spot} - P_{implied} $$
- **Signal:** If $D > 0$, the Spot Price is higher than the Implied Price, suggesting a potential arbitrage or signal misalignment.

## Project Structure
- `arbitrage_analysis.ipynb`: The core analysis engine containing data fetching, parsing, calculation, backtesting, and visualization.

## Setup Instructions

### Prerequisites
- Python 3.8+
- Jupyter Notebook

### Installation
1. Install the required dependencies:
   ```bash
   pip install ccxt pandas plotly requests notebook
   ```

2. Run the Jupyter Notebook:
   ```bash
   jupyter notebook arbitrage_analysis.ipynb
   ```
