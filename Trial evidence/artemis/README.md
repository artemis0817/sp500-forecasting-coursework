# Artemis Trial 1–4 evidence

Each ZIP contains source snapshots, model inputs, fitted OLS coefficients, frozen forecasts, validation records, and Python scripts. Open `04_forecasts/forecast_comparison.csv` inside the relevant trial directory to see the three forecasts.

| Trial | Information cutoff (GMT) | Target close (GMT) |
|---|---|---|
| [1](Artemis_Trial_01_20261102_Evidence.zip) | 2026-11-02 12:00 | 2026-11-09 21:00 |
| [2](Artemis_Trial_02_20261103_Evidence.zip) | 2026-11-03 12:00 | 2026-11-10 21:00 |
| [3](Artemis_Trial_03_20261104_Evidence.zip) | 2026-11-04 12:00 | 2026-11-11 21:00 |
| [4](Artemis_Trial_04_20261105_Evidence.zip) | 2026-11-05 12:00 | 2026-11-12 21:00 |

The three models are Random walk (no drift), Momentum20 only OLS, and Momentum20 + VIX5 OLS. The forecasts were generated after their noon information cutoffs using cutoff-filtered daily close data. The forecast records preserve the actual run times.

[ARCHIVE_MANIFEST.json](ARCHIVE_MANIFEST.json) lists the SHA-256 hashes, run times, and recorded forecasts. All four ZIPs passed integrity checks and match the archives in the earlier combined package byte for byte.
