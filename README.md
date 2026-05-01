# 🚀 Binance Futures Testnet Trading Bot

A simple and structured Python-based CLI trading bot that places **Market** and **Limit** orders on the Binance Futures Testnet (USDT-M).

This project was built as part of a Python Developer Intern assignment.

## 📌 Features

* ✅ Place **MARKET** and **LIMIT** orders
* ✅ Supports both **BUY** and **SELL**
* ✅ Command Line Interface (CLI) input
* ✅ Input validation and error handling
* ✅ Logging of API requests, responses, and errors
* ✅ Clean and modular project structure

## 🛠️ Tech Stack

* Python 3.x
* python-binance
* argparse
* logging
* dotenv


## 📂 Project Structure

```
trading_bot/
│
├── bot/
│   ├── client.py          # Binance API client
│   ├── orders.py          # Order execution logic
│   ├── validators.py      # Input validation
│   ├── logging_config.py  # Logging setup
│
├── cli.py                 # CLI entry point
├── requirements.txt
├── README.md
├── LICENSE
```


## ⚙️ Setup Instructions

### 1. Clone the repository

```
git clone https://github.com/YOUR_USERNAME/trading-bot.git
cd trading-bot
```

### 2. Install dependencies

```
pip install -r requirements.txt
```

### 3. Configure environment variables

Create a `.env` file in the root directory:

```
BINANCE_API_KEY=your_api_key
BINANCE_SECRET_KEY=your_secret_key
```


### 4. Binance Testnet Setup

* Create an account on Binance Futures Testnet
* Generate API keys
* Ensure Testnet is enabled


## ▶️ How to Run

### 🔹 Place MARKET Order

```
python cli.py --symbol BTCUSDT --side BUY --type MARKET --qty 0.01
```

### 🔹 Place LIMIT Order

```
python cli.py --symbol BTCUSDT --side SELL --type LIMIT --qty 0.01 --price 60000
```

## 📊 Sample Output

```
📌 Order Request:
{'symbol': 'BTCUSDT', 'side': 'BUY', 'type': 'MARKET', 'qty': 0.01}

✅ Order Success:
{
  'orderId': 123456,
  'status': 'FILLED',
  'executedQty': '0.01',
  'avgPrice': '60000'
}
```


## 🧾 Logging

* Logs are stored in: `app.log`
* Includes:

  * API requests
  * API responses
  * Errors

## ⚠️ Assumptions

* User provides valid Binance Futures symbols (e.g., BTCUSDT)
* API keys are correctly configured
* Internet connection is stable


## ❌ Error Handling

* Invalid inputs (symbol, side, type, quantity)
* Missing price for LIMIT orders
* API errors (invalid request, insufficient balance)
* Network failures


## 🎯 Bonus (if implemented)

* Improved CLI UX
* Additional order types
* Enhanced logging format


## 📬 Submission

* GitHub repository with source code
* README.md
* requirements.txt
* Log files for:

  * One MARKET order
  * One LIMIT order


## 👨‍💻 Author

MAHALAKSHMI . K


## 📜 License

This project is licensed under the MIT License.
