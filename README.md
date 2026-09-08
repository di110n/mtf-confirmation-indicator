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
- Same-direction or inverse-direction external confirmation
- Optional external trend background for historical verification
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
Final long / short signal
```

Disabled confirmation modules evaluate as allowed, so the indicator can be tested incrementally.

## Project goal

Turn a simple trading rule into a reliable, non-repainting indicator architecture suitable for portfolio use and future client work.

## Next steps

- Validate external-symbol confirmation behavior
- Add invalid HTF selection warning
- Add diagnostics
- Add alerts
- Complete repainting and edge-case tests
- Refactor and package for portfolio use
