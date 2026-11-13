# Orainna Historical Backtesting

This backtest compares a random-walk benchmark with an expanding log-momentum OLS model on the S&P 500 price index. It evaluates 142 Friday 12:00 Europe/London origins from 9 February 2024 to 23 October 2026, with target closes through 30 October 2026.


The target is the latest close available at or before 7 days 9 hours after each origin, in London wall-clock time. Close availability is assumed at 16:00 New York time. This log-return OLS specification is distinct from report C(i), which uses simple returns.

| Model | MAPE | Mean signed error | Mean absolute error |
|---|---:|---:|---:|
| Random walk | 1.606190% | −0.284903% | 100.267049 points |
| Expanding log-momentum OLS | 1.584481% | +0.161803% | 98.726305 points |

The 0.021708 percentage-point MAPE difference is small; overlapping weekly forecasts are serially dependent. It does not establish better future performance.

`Orainna_Backtesting_Support_20261113.zip` contains the Yahoo `^GSPC` snapshot, scripts, per-origin results, independent checks and checksums. The snapshot was retrieved on 31 October 2026 and has no historical publication timestamps, so this is a retrospective backtest. Yahoo is not the official scoring source.

To reproduce, extract the ZIP to a fresh folder and run:

```sh
python3 src/run_validation.py
python3 scripts/recompute_independent_metrics.py
python3 evidence/independent_check.py
```

`ARCHIVE_MANIFEST.json` records the ZIP hash; `INDEPENDENT_METRICS.json` contains an independent Decimal recalculation. No final group model selection or approval is recorded here.
