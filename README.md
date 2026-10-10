# Crypto Arbitrage Monitor

Real-time cryptocurrency arbitrage monitoring web application using FastAPI, CCXT, and WebSockets.

## Run locally

1. Create a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Start the app:
   ```bash
   python main.py
   ```

4. Open in the browser:
   ```text
   http://localhost:8000
   ```

## Features

- Connects to Binance, Bybit, and OKX via CCXT
- Retrieves live ticker data for BTC/USDT
- Compares buy/sell prices across exchanges
- Computes net arbitrage spread, including estimated exchange fees
- Pushes updates over WebSocket every ~1.5 seconds
- Displays a live table and best opportunity card in the browser

## Notes

- The app includes error handling for temporary exchange outages, rate limits, and request timeouts.
- If one exchange is unavailable, the dashboard continues operating with the remaining exchanges.
