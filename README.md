# India-Stocks-2191-2220-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2191 to 2220)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2191-2220-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2191 to 2220)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2191 | `SHREEPUSHK` | Shree Pushkar Chemicals & Fertilisers Limited | `SHREEPUSHK.NS` |
| 2192 | `SHREERAMA` | Shree Rama Multi-Tech Limited | `SHREERAMA.NS` |
| 2193 | `SHRENIK` | Shrenik Limited | `SHRENIK.NS` |
| 2194 | `SHREYANIND` | Shreyans Industries Limited | `SHREYANIND.NS` |
| 2195 | `SHRIKRISH` | Shri Krishna Devcon Limited | `SHRIKRISH.NS` |
| 2196 | `SHRINGARMS` | Shringar House of Mangalsutra Limited | `SHRINGARMS.NS` |
| 2197 | `SHRIRAMPPS` | Shriram Properties Limited | `SHRIRAMPPS.NS` |
| 2198 | `SHRJAGP` | Shri Jagdamba Polymers Limited | `SHRJAGP.NS` |
| 2199 | `SHUKRAPHAR` | Shukra Pharmaceuticals Limited | `SHUKRAPHAR.NS` |
| 2200 | `SHYAMCENT` | Shyam Century Ferrous Limited | `SHYAMCENT.NS` |
| 2201 | `SHYAMTEL` | Shyam Telecom Limited | `SHYAMTEL.NS` |
| 2202 | `SICAGEN` | Sicagen India Limited | `SICAGEN.NS` |
| 2203 | `SICALLOG` | Sical Logistics Limited | `SICALLOG.NS` |
| 2204 | `SIEL` | Superior Industrial Enterprises Limited | `SIEL.NS` |
| 2205 | `SIGACHI` | Sigachi Industries Limited | `SIGACHI.NS` |
| 2206 | `SIGIND` | Signet Industries Limited | `SIGIND.NS` |
| 2207 | `SIGMA` | Sigma Solve Limited | `SIGMA.NS` |
| 2208 | `SIGMAADV` | SIGMA ADVANCED SYSTEMS LIMITED | `SIGMAADV.NS` |
| 2209 | `SIGNPOST` | Signpost India Limited | `SIGNPOST.NS` |
| 2210 | `SIKA` | Sika Interplant Systems Limited | `SIKA.NS` |
| 2211 | `SIKKO` | Sikko Industries Limited | `SIKKO.NS` |
| 2212 | `SIL` | Standard Industries Limited | `SIL.NS` |
| 2213 | `SILGO` | Silgo Retail Limited | `SILGO.NS` |
| 2214 | `SILINV` | SIL Investments Limited | `SILINV.NS` |
| 2215 | `SILVERTUC` | Silver Touch Technologies Limited | `SILVERTUC.NS` |
| 2216 | `SIMBHALS` | Simbhaoli Sugars Limited | `SIMBHALS.NS` |
| 2217 | `SIMPLEXINF` | Simplex Infrastructures Limited | `SIMPLEXINF.NS` |
| 2218 | `SIMPLXREA` | Simplex Realty Limited | `SIMPLXREA.NS` |
| 2219 | `SINCLAIR` | Sinclairs Hotels Limited | `SINCLAIR.NS` |
| 2220 | `SINDHUTRAD` | Sindhu Trade Links Limited | `SINDHUTRAD.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream SHREEPUSHK 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2191-2220-Historical-Data/main/SHREEPUSHK/1m/2026/10/SHREEPUSHK_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
