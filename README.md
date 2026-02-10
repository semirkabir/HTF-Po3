# $ - HTF Sweeps & PO3 Indicator

## Overview

**HTF Sweeps & PO3** is a professional-grade Pine Script indicator for TradingView designed to help traders identify high-probability reversal setups based on **Liquidity Sweeps** and **Power of 3 (PO3)** concepts (Accumulation, Manipulation, Distribution).

This tool visualizes **Higher Timeframe (HTF)** candles directly on your Lower Timeframe (LTF) chart, allowing you to see where HTF liquidity (Previous Highs and Lows) resides without switching timeframes. It automatically detects and highlights "sweeps"—instances where price takes out a key level and immediately reverses, often signaling a manipulation phase before a major move.

## Key Features

### 1. Multi-Timeframe Visualization

- **Overlay HTF Candles:** View up to 3 different higher timeframe candles (e.g., Daily, 4h, 1h) simultaneously on your execution chart (e.g., 5m or 15m).
- **Customizable Style:** Toggle between full candles, just wicks, or simple lines to keep your chart clean.
- **Countdown Timer:** Displays a countdown to the close of the HTF candle directly on the chart.

### 2. Automated Sweep Detection

- **Liquidity Scans:** Automatically identifies when price "sweeps" (takes out) a previous HTF high or low and closes back inside the range.
- **Real-time & Historical:** Draws lines extending from the sweep point to help you track the reaction level.
- **Invalidation Logic:** Smartly invalidates and hides sweep levels once they are decisively breached, reducing chart clutter.

### 3. Precision Entry "Dots"

- **Micro-Structure focus:** Displays discrete "dots" on specific lower timeframes (e.g., 1m, 3m) at key HTF levels.
- **Dynamic Visibility:** Optimized visibility rules ensure dots only appear on relevant lower timeframes to prevent noise (e.g., 4h dots only show on 1m-1h charts).

### 4. Smart Alerts

- **Session-Based Alerts:** Restrict alerts to specific trading sessions (**London**, **New York**) to ignore noise outside key operating hours. Supports Daylight Savings (DST).
- **Event Types:**
  - **Previous H/L:** Alert when price touches a previous HTF candle's high or low.
  - **Sweep Formation:** Alert when a confirmed sweep candle closes (manipulation confirmed).

## Installation

1.  Copy the source code from the `indicator` file.
2.  Open **TradingView**.
3.  Click on **Pine Editor** at the bottom of the screen.
4.  Paste the code into the editor.
5.  Click **"Add to Chart"** or **"Save"**.

## Usage Guide

### General Strategy

This indicator is best used to trade **Reversals** and **Continuations** following a liquidity event.

1.  **Identify the Trend:** Use the HTF candles to see the broader market direction.
2.  **Wait for Liquidity:** Watch for price to approach the High or Low of a previous HTF candle.
3.  **The Sweep (Manipulation):**
    - Look for the indicator to draw a **Sweep Line**. This happens when price pierces the level but fails to close beyond it (or subsequently reverses).
    - This often represents the "Manipulation" phase of the **PO3** cycle.
4.  **Entry:** Look for confirmation on your lower timeframe (e.g., change of character, fair value gap) after the sweep line appears.

### Configuration

The indicator is highly customizable via the specific "HTF" settings groups (HTF1, HTF2, HTF3).

#### HTF Settings (Per Group)

- **Enable:** Toggle the entire group on/off.
- **Display TF:** The higher timeframe to visualize (e.g., `4h`, `D`).
- **Main / HTF Visuals:** Choose how to display lines and sweeps (e.g., `Sweeps`, `Lines`, `Dots`).
- **Extend Sweeps:** Extend the sweep lines to the right for future reference.
- **Stop at Crossover:** Automatically stop drawing the sweep line if price crosses back over it (invalidation).

#### Alerts Settings

- **Session:** Choose to only receive alerts during `London`, `New York`, or both.
- **Previous Candle H/L:** Toggle alerts for simple touches of key levels.
- **Sweep Formation:** Toggle alerts for confirmed sweep patterns.

## Terms of Service

This source code is subject to the terms of the Mozilla Public License 2.0.
