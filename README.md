# ORB Midpoint Trading Strategy (TradingView)

This repository contains a Pine Script v5 implementation of an Opening Range Breakout (ORB)
midpoint retracement strategy with strict risk management and end-of-day exits.

## Strategy Overview
- ORB Range: 09:30–10:00 New York time
- Bias determined by candle CLOSE outside ORB
- Entry via limit order at ORB midpoint
- Fixed take profit
- Dynamic stop-loss based on ORB range
- Maximum trades per day
- Forced EOD exit at 15:45 NY time

## Trade Logic
1. Capture the opening range high/low
2. Determine directional bias using candle close
3. Wait for price retracement to midpoint
4. Enter trade with predefined SL and TP
5. Exit all positions before market close

## Risk Management
- Stop-loss beyond ORB extremes
- Daily trade limit
- Automatic invalidation on range failure

## Files
- `/pine/orb_midpoint_eod.pine` – main strategy code
- `/docs/strategy_explanation.md` – detailed logic explanation

## Disclaimer
This strategy is for educational purposes only. It is not financial advice.
