# Inducement SMC Adaptive — Overlay Indicator

TradingView Pine Script™ v5 **overlay** indicator for detecting **inducement** with a **regime-aware adaptive** system. Works on XAU/USD, crypto, FX, and any other symbol.

## What it does
- Detects swing highs/lows and market structure (BOS / CHoCH).
- Identifies inducement: a sweep of minor liquidity before continuation.
- Filters entries with Fair Value Gaps (FVG), Order Blocks (OB), EMA, ADX, HTF alignment, volume, and session.
- Uses a **confluence score** to only take high-quality setups.
- Detects market **regime** (Trending / Ranging / Volatile) and adapts SL and R:R automatically.
- Supports breakeven stop, trailing stop, and time-based exit.
- Plots BUY/SELL signals with SL/TP lines.
- Tracks winrate statistics in the info panel.
- Provides native TradingView alerts.

## How to use
1. Open [TradingView Pine Editor](https://www.tradingview.com/pine_script/).
2. Copy the entire contents of `inducement_smc.pine`.
3. Click **Save** and **Add to chart**.
4. The indicator appears **on the price chart** by default (overlay). If it opens in a separate lower pane, right-click the indicator name → **Move to** → **Pane above**.
5. Set alerts by right-clicking the indicator → **Add Alert** → choose Long Entry or Short Entry.

## Recommended settings

### XAU/USD
| Setting | Value |
|---|---|
| Timeframe | 15m or 1h |
| Swing Lookback | 5 |
| Inducement Swing Lookback | 3 |
| Use HTF Filter | true |
| HTF Timeframe | 60 |
| Signal Filter Mode | None |
| Use EMA Trend Filter | true |
| EMA Period | 200 |
| Use ADX Filter | true |
| Min ADX | 20 |
| Use Confluence | true |
| Minimum Confluence Score | 60 |
| SL Mode | Fixed percent |
| SL Percent | 0.3 |
| Base Risk:Reward | 2.0 |
| Move to Breakeven | true |
| Use Trailing Stop | true |

### Crypto (BTC, altcoins)
| Setting | Value |
|---|---|
| Timeframe | 15m or 1h |
| Use HTF Filter | true |
| HTF Timeframe | 240 or 60 |
| SL Mode | Fixed percent |
| SL Percent | 0.3 to 0.5 |
| Base Risk:Reward | 2.0 |
| Use Confluence | true |
| Minimum Confluence Score | 60 |

## Winrate improvement tips
- Use **Fixed percent SL** for consistent R:R on any symbol.
- Enable **HTF Filter** — only trade with the higher-timeframe trend.
- Enable **ADX Filter** and **Confluence Score** — skip low-quality setups.
- Enable **Breakeven** and **Trailing Stop** — protect capital and let winners run.
- Use **Session Filter** for XAU/USD to avoid low-liquidity periods.

## Files
- `inducement_smc.pine` — Pine Script v5 overlay source code.
- `README.md` — this file.
- `inducement_tailbar.html` — Mongolian explanation with chart examples.

## Disclaimer
This indicator is for educational and analytical purposes only. It is not financial advice. Always backtest and use proper risk management.
