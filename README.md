# Inducement + SMC Entry Indicator

TradingView Pine Script™ v5 indicator for detecting **inducement** on XAU/USD and any other pair.

## What it does
- Detects swing highs/lows and market structure (BOS / CHoCH).
- Identifies inducement: a sweep of minor liquidity before continuation.
- Filters entries with Fair Value Gaps (FVG) and Order Blocks (OB).
- Plots BUY/SELL signals with ATR-based stop-loss and take-profit lines.
- **Show Only Entry Signals** mode: hides swing points, BOS/CHoCH, and inducement labels so only BUY/SELL signals remain.
- **Winrate statistics** in the info panel: winrate %, average win/loss in pips for long, short, and total.
- Provides native TradingView alerts.

## How to use
1. Open [TradingView Pine Editor](https://www.tradingview.com/pine_script/).
2. Copy the entire contents of `inducement_smc.pine`.
3. Click **Save** and **Add to chart**.
4. Set alerts:
   - Right-click the indicator → **Add Alert**.
   - Choose condition `Inducement + SMC Entry [XAU/USD & Pairs]`.
   - Select **Long Entry** or **Short Entry**.

## Recommended XAU/USD settings
- Timeframe: 15m or 1h
- Swing Lookback: 5
- Inducement Swing Lookback: 3
- ATR Period: 14
- ATR Multiplier: 1.5
- Risk:Reward: 2.0

## Files
- `inducement_smc.pine` — Pine Script v5 source code.
- `README.md` — this file.

## Disclaimer
This indicator is for educational and analytical purposes only. It is not financial advice. Always backtest and use proper risk management.
