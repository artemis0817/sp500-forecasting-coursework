# Artemis historical backtesting

This archive supports the report's historical comparison of rolling-window Momentum OLS and Momentum plus VIX OLS (C(ii) and D). It also includes the unchanged-close benchmark and historical drift diagnostic. The 103 weekly forecast origins were evaluated using three-year rolling fits with matured outcomes. The nine VIX windows use the same evaluation origins. VIX5 had the lowest MAPE among the VIX variants (1.6737%). Momentum-only OLS recorded 1.6639%.

See results/backtest_predictions.csv and results/metrics.csv for the initial comparison. See vix_window_2_to_10/vix_window_ranking.csv and backtest_predictions_vix2_to_10.csv in that directory for the sensitivity results.

Extract the ZIP to a separate working directory. Install the versions in requirements.txt and run python run_model.py, then python validate_results.py. For the VIX comparison run python run_vix_window_comparison.py --windows 2 3 4 5 6 7 8 9 10 --output-subdir vix_window_reproduction. The scripts use saved Yahoo Finance S&P 500 and Cboe VIX snapshots. Historical first-publication timestamps and data vintages were not independently verified. Source redistribution terms apply.

ARCHIVE_MANIFEST.json records the archive checksum.
