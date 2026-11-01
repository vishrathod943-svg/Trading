# NSE cash stocks: 2026 five-minute OHLCV, in parts

**PARTIAL COVERAGE: January 1–April 30, 2026 only.** This contains 214 cash stocks from the source F&O-underlying universe, not every NSE-listed stock. May–October 2026 are absent.

Nine independent ZIP files contain one ordinary CSV per stock: 25 stocks per part, with 14 in the last part. No joining is required. Each ZIP includes its coverage report and source notes.

| Part | Download | Stocks | Alphabetical range | 5-minute bars |
|---|---|---:|---|---:|
| 1 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part01.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part01.zip) | 25 | 360ONE – BAJFINANCE | 150,000 |
| 2 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part02.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part02.zip) | 25 | BALKRISIND – COLPAL | 150,000 |
| 3 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part03.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part03.zip) | 25 | CONCOR – GRASIM | 150,000 |
| 4 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part04.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part04.zip) | 25 | HAL – INOXWIND | 150,000 |
| 5 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part05.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part05.zip) | 25 | IOC – MANAPPURAM | 150,000 |
| 6 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part06.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part06.zip) | 25 | MANKIND – OIL | 150,000 |
| 7 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part07.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part07.zip) | 25 | ONGC – SAMMAANCAP | 150,000 |
| 8 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part08.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part08.zip) | 25 | SBICARD – TRENT | 150,000 |
| 9 | [NSE_cash_5min_2026_Jan-Apr_PARTIAL_part09.zip](parts/NSE_cash_5min_2026_Jan-Apr_PARTIAL_part09.zip) | 14 | TVSMOTOR – ZYDUSLIFE | 83,997 |

Total: **214 stocks, 1,283,997 bars.** [Coverage by stock](coverage.csv). [ZIP checksums and symbol lists](parts_manifest.json).

The earlier `NSE_cash_first25_5min_2026_Jan-Apr_PARTIAL.zip` contains the same first 25 stocks as part 1; it is retained for the existing download link.

# NSE cash stocks: partial 2026 five-minute OHLCV

PARTIAL DATA: 214 stocks from a third-party F&O-underlying cash-stock dataset.
This is NOT all NSE-listed stocks and NOT complete 2026 year-to-date coverage.
The source ends on 2026-04-30. May through October 2026 are absent.
Each stock's actual first/last timestamp and row counts appear in coverage.csv.

Source and credits: voletiramu, https://github.com/voletiramu/nse-fno-1min-data/releases/tag/v1.0.0
Source reports Zerodha Kite cash/spot data; this was not independently reconciled to NSE.
Source archive SHA256: 20024713c455cc16b5daae91e06991d57a1acfa6a30c77bb7d5a742ee1789ab2
Use: research/education, AS-IS; upstream says not for commercial redistribution.

Files: one ordinary CSV per stock under csv/.
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
