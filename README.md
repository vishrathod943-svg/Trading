# NSE cash stocks: partial 2026 five-minute OHLCV

PARTIAL DATA: The first 25 stocks alphabetically from a third-party 214-stock F&O-underlying cash-stock dataset.
This is NOT all NSE-listed stocks and NOT complete 2026 year-to-date coverage.
The source ends on 2026-04-30. May through October 2026 are absent.
Each stock's actual first/last timestamp and row counts appear in coverage.csv.

Source and credits: voletiramu, https://github.com/voletiramu/nse-fno-1min-data/releases/tag/v1.0.0
Source reports Zerodha Kite cash/spot data; this was not independently reconciled to NSE.
Source archive SHA256: 20024713c455cc16b5daae91e06991d57a1acfa6a30c77bb7d5a742ee1789ab2
Use: research/education, AS-IS; upstream says not for commercial redistribution.

Files: one ordinary CSV per stock under csv/.
Download all 25 CSVs in NSE_cash_first25_5min_2026_Jan-Apr_PARTIAL.zip.
Included symbols: 360ONE, AARTIIND, ABB, ABCAPITAL, ADANIENSOL, ADANIENT, ADANIGREEN, ADANIPORTS, ADANIPOWER, ALKEM, AMBER, AMBUJACEM, ANGELONE, APLAPOLLO, APOLLOHOSP, ASHOKLEY, ASIANPAINT, ASTRAL, AUBANK, AUROPHARMA, AXISBANK, BAJAJ-AUTO, BAJAJFINSV, BAJAJHLDNG, BAJFINANCE.
Columns: timestamp, open, high, low, close, volume, source_minutes.
Prices: INR, preserved as supplied; corporate-action adjustment status unverified.
Volume: shares as reported by source, summed over each five-minute interval.
Timestamps: Asia/Kolkata (UTC+05:30), interval start, [start, start+5min).
Aggregation: first open, maximum high, minimum low, last close, sum volume.
source_minutes counts observed minute bars; fewer than 5 may indicate missing bars
or partial sessions. No rows are filled, interpolated, or synthesized.
Only source timestamps in calendar year 2026 were retained. Nonempty five-minute
bins are emitted, including any special-session timestamps supplied by the source.
Checks: unique source timestamps, non-null and internally consistent OHLC,
nonnegative volume, 1–5 source minutes per bar, exact volume-total conservation.
These checks do not establish exchange-level accuracy or completeness.
