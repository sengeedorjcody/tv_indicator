# Inducement SMC Entry — Overlay Indicator

TradingView Pine Script™ v5 **overlay** indicator for detecting **inducement** on XAU/USD and any other pair. By default it appears directly on the price chart.

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
4. The indicator must appear **on the price chart** (overlay). If it opens in a separate lower pane, right-click the indicator name → **Move to** → **Pane above**.
5. Set alerts:
   - Right-click the indicator → **Add Alert**.
   - Choose condition `Inducement + SMC Entry [XAU/USD & Pairs]`.
   - Select **Long Entry** or **Short Entry**.

## Recommended XAU/USD settings
- Timeframe: 15m or 1h
- Swing Lookback: 5
- Inducement Swing Lookback: 3
- Signal Filter Mode: None
- Use EMA Trend Filter: true
- EMA Period: 200
- Wait for Candle Close Confirmation: true
- SL Mode: Inducement level
- ATR Period: 14
- ATR Multiplier: 1.0
- Max SL in pips: 50
- Risk:Reward: 2.0

## Winrate improvement tips
- Use **Inducement level SL** instead of ATR-based SL — places stop below/above the inducement sweep.
- Enable **EMA Trend Filter** — only trade in the direction of the 200 EMA.
- Enable **Candle Close Confirmation** — avoids false breakout entries.
- Keep **Max SL in pips** tight enough for your pair (e.g., 50 pips for XAU/USD).

## Files
- `inducement_smc.pine` — Pine Script v5 overlay source code.
- `README.md` — this file.
- `inducement_tailbar.html` — Mongolian explanation with chart examples.

## Disclaimer
This indicator is for educational and analytical purposes only. It is not financial advice. Always backtest and use proper risk management.
