
# Binance Trading Bot

## Overview

This Binance trading bot is a Python application that uses the Binance API for executing trades based on predefined strategies. The bot includes functionalities to monitor token prices, analyze trading pairs, and execute buy/sell actions accordingly.

## Prerequisites

Before running the bot, make sure you have the following:

- Python 3.6 or higher installed
- Binance API key and secret
- Moralis API key (for token price monitoring)

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/binance-trading-bot.git
Install dependencies:

Copy code
    ```bash
    pip install -r requirements.txt

2. Install dependencies:

   ```bash
   pip install -r requirements.txt

3. Create a .env file in the project root and add your Binance and Moralis API keys:

   ```bash
   MORALIS_API_KEY="your_moralis_api_key"

4. Configure settings.json with your Binance API keys, target tokens, and other settings.

5. Run the Flask app:

   ```bash
   python app.py
The app will run on http://localhost:5002







## Files and Directories

- app.py: Flask web application to retrieve token prices from the Moralis API and handle webhooks for trade execution.
- binance_connect.py: Module for interacting with the Binance API, including querying account information, retrieving candlestick data, and executing trades.
- execute.py: Module containing functions for executing trades based on predefined strategies.
- strategy.py: Module with functions for analyzing trading pairs and determining buy/sell decisions.
- eth_pair.json: JSON file containing information about a specific trading pair (e.g., ETH/BTC) for configuration purposes.
- settings.json: JSON file for storing Binance API keys, target tokens, and other project settings.




## Running the Bot

1. Ensure the Flask app is running (python app.py).

2. Run the trading bot:
  
   ```bash
   python execute.py

The bot will continuously check for trading opportunities and execute trades based on predefined strategies.

## Additional Strategy

A new strategy has been added to the execute.py file. This strategy checks the price of a specific coin (e.g., ETH) every minute. If the price falls below a certain threshold, the bot will execute a buy action.


To customize the threshold and target coin, modify the

   ```bash
   check_price_condition_and_trade function in execute.py
   ```
Feel free to update the code
   ```bash
   Replace `"your_moralis_api_key"` with your actual Moralis API key and update any other project-specific details. Save this content in your `README.md` file within the root directory of your project.
```

## Authors

- [obylo98](https://www.github.com/obylo98)
- [ugohuche](https://github.com/ugohuche)
