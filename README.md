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
- External confirmation is intended for chart timeframe or higher; lower external timeframes are not part of the v1 support contract
- Same-direction or inverse-direction external confirmation
- Optional external trend background for historical verification
- Shared bullish/bearish background colors and transparency controls
- HTF filter automatically disables when the selected HTF is equal to or lower than the chart timeframe, with a clear chart warning
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

## Validation status

Verified in TradingView:

- HTF confirmation behavior on lower chart timeframes
- HTF warning display
- Long and short alert conditions appear in the alert dialog
- External higher-timeframe confirmation on a 1m chart with 5m external data
- External background changes on 5m boundaries
- Historical external states remained stable after reload

## Next steps

- Run the final acceptance-test sweep
- Capture clean portfolio screenshots
- Finalize the client-facing project description
- Freeze and package the Week 1 version
