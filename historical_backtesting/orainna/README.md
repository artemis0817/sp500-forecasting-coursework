# Orainna historical backtesting — interim log-return OLS

## Scope
This package reproduces the saved Orainna interim backtest for two models: the unchanged-price random-walk benchmark and an expanding-window, one-factor momentum OLS model. It is a contributor evidence package for `historical_backtesting/orainna/`, prepared on 13 November 2026. It is not a final coursework forecast, model selection, or group approval.

This OLS variant uses log returns. The report's C(i) is an expanding simple-return OLS model. Treat these as distinct specifications unless the group formally reconciles them. This package does not claim to cover all five group model variants or add a Fixed Momentum result.

## Exact model definitions
At a Friday 12:00 Europe/London origin, let `P_t` be the latest S&P 500 close assumed available by the origin and `m20_t = ln(P_t / P_{t-20})`, using the close 20 exchange sessions earlier. The target is the latest S&P 500 close available at or before the origin plus 7 days and 9 hours in Europe/London wall-clock time. The realized training label is `y_t = ln(P_target / P_t)`.

- **Random walk:** `F_t = P_t`.
- **Orainna expanding log-momentum OLS:** fit `y_i = a + b m20_i + error_i` by OLS on all prior Friday-origin observations whose target close was already observed by the current origin. The training window expands over time. The model is used only after at least 52 matured training labels. Forecast: `F_t = P_t × exp(a + b m20_t)`.

The script treats a daily close as available at 16:00 America/New_York on its session date. This is an exchange-close assumption, not a verified Yahoo publication timestamp. Labels whose close time is after the current origin are excluded. The horizon follows London wall-clock time, so UTC duration varies around DST changes.

## Results
Frozen input: Yahoo Finance `^GSPC` chart snapshot retrieved 31 October 2026 at 15:07:57 UTC, with closes through 30 October. The test covers 142 eligible origins from 9 February 2024 to 23 October 2026; target closes run through 30 October 2026.

| Model | MAPE | Mean signed percentage error | Mean absolute point error |
|---|---:|---:|---:|
| Random walk | 1.606190% | −0.284903% | 100.267049 |
| Expanding log-momentum OLS | 1.584481% | +0.161803% | 98.726305 |

The MAPE difference is about 0.021708 percentage points on this sample. Weekly forecast horizons overlap and remain serially dependent; these figures do not establish that OLS generalizes better.

## Reproduction
Extract `Orainna_Backtesting_Support_20261113.zip` into a new scratch folder. From the extracted `Orainna_Backtesting_Support_20261113/` directory, run:

```sh
python3 src/run_validation.py
python3 scripts/recompute_independent_metrics.py
python3 evidence/independent_check.py
```

Python 3.9+; standard library only; no network or online AI required. `evidence/verification_run.txt` records observed outputs. `SHA256.json` covers package files other than itself. The top-level `ARCHIVE_MANIFEST.json` records the ZIP hash.

## Source and limits
The input is a third-party Yahoo Finance series, not the official S&P Dow Jones marking feed. The saved response does not contain exact first-publication timestamps or historical vintages. The backtest uses a frozen later-retrieved/current-vintage historical series with the exchange-close availability assumption above. This is retrospective and does not prove each value was available at each historical origin. Recheck the official reference series and group-approved model before final submission.

The Yahoo snapshot is included for offline reproduction. Provider redistribution terms have not been determined in this package; review them before placing the archive in a public repository. No credentials or unrelated personal files are included.
