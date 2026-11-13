# Orainna — Trial 1–4 evidence

The folder and archive names follow the repository convention used by `artemis/` and `zaf/`: lowercase contributor folder, then one archive for each trial, dated with the original trial date.

Each ZIP contains the byte-identical original frozen trial archive, Orainna’s later Yahoo-based reconstruction of the two comparison rows, model inputs and coefficients, forecast and error records, source/timing notes, code, software versions, saved command output, checksums, and offline reproduction instructions. Extract a ZIP and read its `README.md`. `ARCHIVE_MANIFEST.json` records each archive SHA-256, the preserved original freeze hash, and reproduced forecast values.

These four packages were prepared on 13 November 2026. They are retrospective reconstructions, not forecasts issued at the original cutoffs. All four source captures were after their stated noon cutoffs. Calculations rebuild from the raw Yahoo JSON in each preserved freeze; those raw-file hashes match the original archive manifests. A separate aggregate-sum OLS calculation reproduces each Momentum20-only result.

The later target closes were transcribed from a Yahoo historical page view; the page HTML and screenshot were not retained. The ZIPs disclose this capture limitation and record the FRED/AP cross-checks. No group approval is claimed. These Orainna comparison rows cover Momentum20-only OLS and Random walk; they do not replace the coursework’s primary Random walk, Fixed momentum, and Expanding regression models. The completed Orainna workbook is a separate file at the repository root beside this `orainna/` folder.

Original frozen input archives are preserved byte-for-byte. The retrospective comparison adds calculations and later actuals; it does not alter the frozen observations or claim the four-model outputs recorded in Zaf’s packages.
