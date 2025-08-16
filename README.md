# Crypto-Trading-Bot

# 🤖 AI/ML Crypto Trading Bot with LLM-Enhanced Signals

## 📌 Overview
This project is an **automated cryptocurrency trading bot** that:
- Uses **real-time market data** from top exchanges (Binance, Coinbase, KuCoin) via REST + WebSocket APIs
- Combines **machine learning models** for price prediction with **Large Language Models (LLMs)** for signal reasoning and sentiment analysis
- Places **spot** and **futures** trades automatically (limit and market orders supported)
- Includes a **risk management layer** to prevent overexposure
- Supports **paper trading** on exchange testnets before going live

> ⚠️ **Disclaimer**: This bot is for educational purposes only. Cryptocurrency trading carries significant financial risk. Use at your own risk.

---

## 🚀 Features
- **Live Data**: Real-time OHLCV, orderbook, and trade feed via REST & WebSocket
- **LLM Integration**: Summarizes news, social signals, and technical data into structured trading signals
- **Multi-Exchange Support**: Unified API access via [CCXT](https://github.com/ccxt/ccxt)
- **Spot & Futures Trading**: Configurable leverage, position size, and order types
- **Limit Orders**: Place `limit`, `stop-limit`, `OCO` orders with time-in-force options
- **Backtesting & Simulation**: Validate strategies before live deployment
- **Risk Controls**: Max daily loss, position size limits, cooldown between trades
- **Logging & Alerts**: Trade history, LLM prompts/responses, Telegram/email alerts

---

## 📂 Project Structure
├── data/ # Historical & live market data
├── models/ # ML/LLM models & training scripts
├── strategies/ # Strategy logic & LLM integration
├── exchange/ # API clients for Binance, Coinbase, KuCoin
├── risk/ # Risk management & position sizing
├── tests/ # Unit & integration tests
├── main.py # Entry point for running the bot
├── requirements.txt # Python dependencies
└── README.md # Project documentation




---

## 🛠️ Tech Stack
- **Python 3.9+**
- [CCXT](https://github.com/ccxt/ccxt) / [CCXT Pro](https://github.com/ccxt/ccxt.pro) for exchange integration
- [python-binance](https://github.com/sammchardy/python-binance) / exchange SDKs
- **PyTorch** / **TensorFlow** for ML models
- **Transformers** (Hugging Face) for LLM-based reasoning
- **pandas-ta / TA-Lib** for technical indicators
- **vectorbt** for backtesting
- **LangChain** for LLM orchestration

---

## 📡 Setup & Installation
### 1. Clone the repository

git clone https://github.com/<your-username>/ai-ml-trading-bot.git
cd ai-ml-trading-bot


### 2.Create a virtual environment & install dependencies
python3 -m venv venv
source venv/bin/activate  # (Windows: venv\Scripts\activate)
pip install -r requirements.txt

### 3.Set up environment variables

BINANCE_API_KEY=your_binance_api_key
BINANCE_API_SECRET=your_binance_api_secret
COINBASE_API_KEY=your_coinbase_api_key
COINBASE_API_SECRET=your_coinbase_api_secret
KUCOIN_API_KEY=your_kucoin_api_key
KUCOIN_API_SECRET=your_kucoin_api_secret
OPENAI_API_KEY=your_openai_api_key
RISK_MAX_POSITION=0.01  # Max position size as fraction of account
RISK_MAX_DAILY_LOSS=0.05  # Max daily loss % before bot stops



### 📈 Strategy Development
ML Models: Use historical OHLCV + orderbook depth to train models (LSTM, transformers, CNNs, etc.)

LLM Signals: Feed latest indicators, market summaries, and news into an LLM prompt

Hybrid Decision: Combine ML probability output with LLM confidence score

Risk Filter: Pass only high-confidence trades to execution layer


### 💡 Future Improvements
Add sentiment analysis from Twitter/Reddit feeds

Implement reinforcement learning strategies

Deploy on cloud (AWS/GCP) with auto-restart & failover

Add GUI dashboard for monitoring bot performance

# 📈 Workflow 


<img width="2928" height="3835" alt="trading-bot" src="https://github.com/user-attachments/assets/9ad8d544-c92a-4b6a-81b1-8726a390587d" />
