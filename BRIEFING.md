# Apple Inc. (AAPL) — One-Page Diligence Brief

_Prepared for the Thursday investment-club meeting. Every figure below was pulled from live lookups at drafting time (Yahoo Finance, Google Maps, Hugging Face Hub) — nothing from memory._

---

## 1. Company Profile

| Field | Value (as returned by the live lookup) |
|---|---|
| **Sector** | Technology |
| **Industry** | Consumer Electronics |
| **Headquarters (address)** | One Apple Park Way, MS 927-4GC, Cupertino, CA 95014, United States |
| **Website** | https://www.apple.com |

**Additional lookup fields:** founded 1976 (formerly Apple Computer, Inc.; renamed Apple Inc. in January 2007), full-time employees 167,000, IR site http://investor.apple.com/.

**Snapshot at time of lookup:** quote price $344.17 USD · market cap ≈ $5.0T · trailing P/E ≈ 38.9 · forward P/E ≈ 32.3 · dividend yield ≈ 0.31% (forward) / 0.47% (5-yr avg) · dividend rate $1.08/yr · trailing-12-month dividend rate $1.06 · payout ratio ≈ 11.8%.

---

## 2. Dividend & Stock-Split History

**Most recent dividend per share: $0.27** — per the live dividend record, paid on 2026-08-10 (prior quarterly entries were $0.26 on 2026-05-11 and 2026-02-09; quarterly faster pace: dividend rate $1.08/yr; trailing-12-month rate $1.06).

**Latest stock split: 4:1 on 2020-08-31.**

**Full dividend record (per-share, as returned by the lookup):**

| Period | Per-share dividend | Notes |
|---|---|---|
| 1987–1995 | $0.000536 → $0.001071 | Early quarterly payouts (first entry 1987-05-11: $0.000536) |
| 1995–2012 | — | Dividends suspended |
| 2012–2019 | $0.094643 → $0.1925 | Dividend reinstated Aug 2012; annual raise to $0.19 by late 2019 |
| 2020–2025 | $0.205 → $0.25 | Steady annual raises (peaked $0.25 on 2024-05-10 / 2024-08-12 / 2024-11-08) |
| 2026 | $0.26 → $0.27 | Two quarterly $0.27 entries (2026-05-11 and 2026-08-10); latest: 2026-08-10 |

**All stock splits returned by the lookup:**

| Date | Split ratio |
|---|---|
| 1987-06-16 | 2:1 |
| 2000-06-21 | 2:1 |
| 2005-02-28 | 2:1 |
| 2014-06-09 | 7:1 |
| **2020-08-31** | **4:1 (latest)** |

---

## 3. Headquarters Check (Google Maps)

| Field | Value returned by Google Maps |
|---|---|
| Geocode place ID | `ChIJoWuKRgC1j4ARyDLPTK4V7HY` |
| Formatted address (geocode) | Cupertino, CA 95014, USA |
| Coordinates | 37.3318699, -122.0295491 |
| Named place for that record | Apple Inc. – Infinite Loop Campus (phone: (408) 996-1010) |
| Apple Park place ID | `ChIJ_Yjh6Za1j4AR8IgGUZGDDTs` |
| Apple Park formatted address | One Apple Park Way, Cupertino, CA 95014, USA |
| Apple Park coordinates | 37.3346438, -122.008972 |

**Confirmed:** Google Maps places Apple's headquarters in Cupertino, CA 95014, USA, and the Apple Park place returns "One Apple Park Way, Cupertino, CA 95014, USA" (`ChIJ_Yjh6Za1j4AR8IgGUZGDDTs`), matching the corporate HQ address in the profile above. The historic Infinite Loop campus site is adjacent (37.3346438, -122.008972 vs. 37.3318699, -122.0295491).

---

## 4. Model Shortlist — Earnings-Transcript Classifier Prototype

| Model | Parameters | Downloads | Likes | License |
|---|---|---|---|---|
| [google-bert/bert-base-uncased](https://hf.co/google-bert/bert-base-uncased) — classic baseline | 110.1M | 3,285.4M | 3,060 | Apache-2.0 |
| [distilbert/distilbert-base-uncased](https://hf.co/distilbert/distilbert-base-uncased) — fast/lighter | 67.0M | 698.4M | 1,142 | Apache-2.0 |
| [FacebookAI/roberta-base](https://hf.co/FacebookAI/roberta-base) — stronger baseline | 124.7M | 663.4M | 700 | MIT |

All three are English `transformers` fill-mask encoders (AutoModelForMaskedLM, dataset bookcorpus + Wikipedia; last Hub update 19 Feb 2024 on all three).

**Recommendation:** start with `bert-base-uncased` as the classic baseline — it carries the heaviest downloads and likes of the shortlist; `distilbert-base-uncased` (~39% fewer parameters) for a lighter, faster edge; `roberta-base` for an accuracy-vs-compute head-to-head benchmark.

---

*Data sources: Yahoo Finance (AAPL profile, dividend & split actions), Google Maps (address geocoding + place lookup), Hugging Face Hub (model stats). Values are as returned at lookup time; please verify anything critical before the club acts on them.*
