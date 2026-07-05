# AUS200 1d OHLCV Index Historical Data — Free Sample

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Dataset rows](https://img.shields.io/badge/full_dataset-7_838_rows-blue)](https://ork.ad/) [![Updated](https://img.shields.io/badge/weekly_update-every_Sunday-green)](https://ork.ad/) [![Full data on ork.ad](https://img.shields.io/badge/download-ork.ad-orange)](https://ork.ad/)

### → [**Download the full AUS200 dataset on ork.ad**](https://ork.ad/)

**AUS200 1d OHLCV Stock index historical data** — ultra high-quality 1d OHLCV for **Australia 200**. Global cash and extended index sessions — Asia, Europe and US coverage, not US-hours only. Clean `time, open, high, low, close, volume` CSV for backtesting, algorithmic trading and quantitative research.

## Table of contents

- [Why this dataset?](#why-this-dataset)
- [Download sample CSV](#download-sample)
- [GitHub Pages preview](#github-pages)
- [Sample vs full dataset](#sample-vs-full-dataset)
- [Timeframes on ork.ad](#timeframes-on-orkad)
- [Weekly updates](#weekly-updates)
- [Data preview](#data-preview)
- [Schema](#schema)
- [Code examples](#code-examples)
- [Download full data on ork.ad](#download-full-data)

## Why this dataset?

- **Ultra high-quality 1d OHLCV** for **Australia 200** (Stock index)
- **Global cash and extended index sessions — Asia, Europe and US coverage, not US-hours only**
- **Clean CSV schema** — `time, open, high, low, close, volume` (no gaps in formatting)
- **Free evaluation sample** on GitHub (`1d`) · **13 timeframes** on [ork.ad](https://ork.ad/) · **7,838** `1d` rows in the full archive
- Built for **backtesting**, **algorithmic trading** and **quantitative finance** workflows
- **Weekly refresh** — [ork.ad](https://ork.ad/) every **Sunday**; GitHub `1d` sample updated in sync

> **Sample on GitHub** · `AUS200_1d.csv` (513 rows, `2024-07-04` → `2026-07-04`). **Full archive on [ork.ad](https://ork.ad/)** — **7,838** `1d` rows (~0.3 MB), **13 timeframes** (``1m`, `3m`, `5m`, `15m`, `30m`, `1H`, `2H`, `4H`, `8H`, `12H`, `16H`, `1D`, `1W``), `1992-06-01` → `2026-07-04`.

## Download sample

**[AUS200_1d.csv](https://github.com/ork-ad/aus200-1d-ohlcv-index-historical-data/blob/main/AUS200_1d.csv)** on GitHub ([raw CSV](https://raw.githubusercontent.com/ork-ad/aus200-1d-ohlcv-index-historical-data/main/AUS200_1d.csv)) · [GitHub Releases](https://github.com/ork-ad/aus200-1d-ohlcv-index-historical-data/releases) when the release workflow is active.

## GitHub Pages

Interactive chart & stats: **[https://ork-ad.github.io/aus200-1d-ohlcv-index-historical-data/](https://ork-ad.github.io/aus200-1d-ohlcv-index-historical-data/)**

## Sample vs full dataset

| | **Sample (this repo)** | **Full dataset ([ork.ad](https://ork.ad/))** |
|---|--:|---|
| Instrument | Australia 200 · Stock index | Australia 200 · Stock index |
| Timeframes | `1d` (sample) | **13** — `1m`, `3m`, `5m`, `15m`, `30m`, `1H`, `2H`, `4H`, `8H`, `12H`, `16H`, `1D`, `1W` |
| 1d rows | 513 | **7,838** |
| Size | 0.02 MB | ~0.3 MB |
| Period | `2024-07-04` → `2026-07-04` | `1992-06-01` → `2026-07-04` |
| File | `AUS200_1d.csv` | ZIP on [ork.ad](https://ork.ad/) |
| Updates | Weekly (Sunday) — GitHub sample | Weekly (Sunday) — all timeframes |

## Timeframes on ork.ad

This GitHub repository ships a **`1d` evaluation sample** only. On **[ork.ad](https://ork.ad/)**, each full asset archive is delivered as a ZIP with **13 gap-free OHLCV timeframes** (one CSV per timeframe):

**1m** · **3m** · **5m** · **15m** · **30m** · **1H** · **2H** · **4H** · **8H** · **12H** · **16H** · **1D** · **1W**

GitHub = `1d` sample · [ork.ad](https://ork.ad/) = all **13** timeframes above for the same instrument.

## Weekly updates

- **[ork.ad](https://ork.ad/)** — Full datasets on ork.ad are updated every Sunday.
- **GitHub (this repo)** — GitHub samples are refreshed weekly (every Sunday), in sync with ork.ad.

When a new `1d` sample is published on GitHub, the README, chart preview and CSV reflect the latest week of data.

## Data preview

First and latest rows from the GitHub sample **`AUS200_1d.csv`**:

**First rows**

| time | open | high | low | close | volume |
| --- | --- | --- | --- | --- | --- |
| 2024-07-04 | 7824.7 | 7856.17 | 7823.65 | 7828.94 | 6414 |
| 2024-07-05 | 7828.94 | 7846.15 | 7795.13 | 7825.64 | 15461 |
| 2024-07-08 | 7825.64 | 7834.5 | 7772.4 | 7792.8 | 10900 |
| 2024-07-09 | 7792.8 | 7848.77 | 7780.86 | 7800.86 | 13131 |
| 2024-07-10 | 7800.86 | 7907.34 | 7792.71 | 7903.33 | 10368 |

**Last rows**

| time | open | high | low | close | volume |
| --- | --- | --- | --- | --- | --- |
| time | open | high | low | close | volume |
| 2026-06-30 | 8837.12 | 8847.41 | 8776.9 | 8799.19 | 20440 |
| 2026-07-01 | 8799.19 | 8801.52 | 8681.11 | 8701.61 | 24244 |
| 2026-07-02 | 8701.61 | 8827.31 | 8668.69 | 8772.09 | 35150 |
| 2026-07-03 | 8772.09 | 8860.65 | 8757.62 | 8805.23 | 10815 |

## Schema

```text
time,open,high,low,close,volume
```

## Code examples

### pandas

```python
import pandas as pd

df = pd.read_csv('AUS200_1d.csv', parse_dates=['time'])
df.set_index('time', inplace=True)
print(df.describe())
print(df.resample('1D').agg({'open': 'first', 'high': 'max',
                              'low': 'min', 'close': 'last', 'volume': 'sum'}).head())
```

### backtrader

```python
import backtrader as bt
import pandas as pd

df = pd.read_csv('AUS200_1d.csv', parse_dates=['time'])
df.set_index('time', inplace=True)

class PandasData(bt.feeds.PandasData):
    params = (('datetime', None), ('open', 'open'), ('high', 'high'),
              ('low', 'low'), ('close', 'close'), ('volume', 'volume'))

cerebro = bt.Cerebro()
cerebro.adddata(PandasData(dataname=df))
# cerebro.addstrategy(YourStrategy)
# cerebro.run()
```

### vectorbt

```python
import pandas as pd
import vectorbt as vbt

df = pd.read_csv('AUS200_1d.csv', parse_dates=['time'])
close = df.set_index('time')['close']
fast, slow = vbt.MA.run(close, 10), vbt.MA.run(close, 50)
entries = fast.ma_crossed_above(slow)
exits = fast.ma_crossed_below(slow)
pf = vbt.Portfolio.from_signals(close, entries, exits, init_cash=10_000, freq='1D')
print(pf.stats())
```

## Download full data

The complete **AUS200** archive on **[ork.ad](https://ork.ad/)** includes **13 OHLCV timeframes** (`1m`, `3m`, `5m`, `15m`, `30m`, `1H`, `2H`, `4H`, `8H`, `12H`, `16H`, `1D`, `1W`) — **7,838** rows at `1d`, plus all other timeframes in the same ZIP.

**[→ Get the full AUS200 dataset on ork.ad](https://ork.ad/)**

---
*GetData · AUS200 1d OHLCV sample on GitHub · Full historical data on [ork.ad](https://ork.ad/) · 2026-07-05 UTC*