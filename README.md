# Repository & Tools Overview

## 1. Ego Calculator
Ego Calculator is a fun and insightful web tool that helps you measure your ego balance—how confident, humble, or self-centered you are. By answering personality-based questions, you’ll discover where you fall between self-assurance and overconfidence, promoting self-awareness and emotional growth.

---

## 2. Equal Highs & Lows Liquidity Indicator (`Equal_Highs_Lows_Liquidity.pine`)
A TradingView Pine Script (v6) indicator designed for Smart Money Concepts (SMC) and Price Action traders to automatically detect and visualize **Equal Highs (EQH / Buy-side Liquidity)** and **Equal Lows (EQL / Sell-side Liquidity)** pools.

### Features
- **Pivot High & Low Detection**: Identifies structural pivot points with customizable left and right lookback lengths.
- **Flexible Tolerance Modes**: Detect equal levels using:
  - **ATR Multiplier**: Adaptable to changing market volatility.
  - **Ticks / Points**: Precise tick or pip threshold (e.g. 20 ticks = 2.0 pips).
  - **Percentage (%)**: Percentage-based price difference.
- **Visual Liquidity Pools**:
  - Horizontal liquidity lines extending to current price bars.
  - Optional shaded liquidity zones (boxes) framing the equal high/low range.
  - Informative price labels tagged as `EQH (BSL)` or `EQL (SSL)`.
- **Sweep & Liquidity Raid Tracking**:
  - Monitors real-time price action for liquidity sweeps (price breaking above EQH or below EQL).
  - Dynamically updates visual styling (dashed gray lines / checkmarks) upon liquidity sweep, or hides swept levels if configured.
- **Alert System**:
  - Real-time alerts when new EQH or EQL liquidity pools form.
  - Sweep alerts when Buy-side Liquidity (BSL) or Sell-side Liquidity (SSL) is raided.

### Pine Script v6 Compliance
- Uses `//@version=6`.
- Ensures history-referencing calculations (`ta.pivothigh`, `ta.pivotlow`, `ta.atr`) run strictly in global scope.
- Avoids deprecated color constants (e.g., `color.darkgreen`), employing valid color constructors and constants.
