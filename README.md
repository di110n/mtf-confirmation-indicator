# MTF Confirmation Indicator

A TradingView Pine Script v6 indicator project focused on deterministic, testable multi-timeframe signal confirmation.

## Current status

The project now includes:

- Configurable fast/slow moving-average base signal
- EMA/SMA selection for the base signal
- Confirmed-bar crossover signals
- Higher-timeframe confirmation
- Confirmed HTF values using the previous completed HTF bar
- Optional HTF trend background for visual verification
- Optional external-symbol confirmation
- Confirmed external values when the selected external timeframe is higher than the chart timeframe
- Same-direction or inverse-direction external confirmation
- Optional external trend background for historical verification
- Shared bullish/bearish background colors and transparency controls
- Warning when the selected HTF is equal to or lower than the chart timeframe
- Long and short alert conditions that match the plotted signals
- Clean grouped inputs
- Distinct fast/slow MA colors

## Signal architecture

```text
Base MA crossover
        ↓
Higher-timeframe confirmation
        ↓
External-symbol confirmation
        ↓
Confirmed chart bar
        ↓
Final long / short signal
        ↓
TradingView alert conditions
```

Disabled confirmation modules evaluate as allowed, so the indicator can be tested incrementally.

## Project goal

Turn a simple trading rule into a reliable, non-repainting indicator architecture suitable for portfolio use and future client work.

## Next steps

- Compile and verify the new display settings, HTF warning, and alerts in TradingView
- Complete the acceptance-test matrix
- Verify historical reload and realtime behavior
- Final README cleanup and screenshots
- Refactor and package the Week 1 version for portfolio use
