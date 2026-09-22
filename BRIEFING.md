# Apple Inc. (AAPL) — One-Page Diligence Brief

_Prepared for the Thursday investment-club meeting. All figures below were pulled from live lookups (Yahoo Finance, Google Maps, Hugging Face) at the time of drafting — no numbers from memory._

---

## 1. Company Profile

| Field | Value |
|---|---|
| **Company** | Apple Inc. (AAPL) |
| **Sector** | Technology |
| **Industry** | Consumer Electronics |
| **Headquarters** | One Apple Park Way, Cupertino, CA 95014, United States |
| **Website** | https://www.apple.com |

**Snapshot at time of lookup:** price $340.97 USD · market cap ~$4.98T · full-time employees 150,000 · founded 1976 (formerly Apple Computer, Inc.; renamed Apple Inc. in January 2007).

---

## 2. Dividend & Stock-Split History

**Most recent dividend per share:** $0.27 (paid 2026-08-10, per the live dividend record). Forward dividend rate: $1.08/year; trailing 12-month rate: $1.05; yield ~0.32%.

**Latest stock split:** 4:1, effective 2020-08-31.

**Full dividend & split record (per-share, as returned by the lookup):**

| Period | Dividend per share | Notes |
|---|---|---|
| 1987–1995 | $0.000536 → $0.001071 | Early quarterly payouts |
| 1995–2012 | none | Dividends suspended |
| 2012–2019 | $0.094643 → $0.1925 | Dividend reinstated Aug 2012 |
| 2019–2024 | $0.205 → $0.25 | Steady annual raises |
| 2024–2025 | $0.26 | |
| **2026 (latest)** | **$0.27** | Most recent quarterly dividend |

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
| **Place ID** | `ChIJ_Yjh6Za1j4AR8IgGUZGDDTs` |
| **Formatted address** | One Apple Park Way, Cupertino, CA 95014, USA |
| **Place name** | Apple Park |
| **Coordinates** | 37.3346438, -122.008972 |

Confirmed: Google Maps places Apple's headquarters (Apple Park) at One Apple Park Way, Cupertino, CA 95014, USA — matching the corporate address in the profile above. (For reference, the historic Infinite Loop campus also sits in Cupertino.)

---

## 4. Model Shortlist — Earnings-Transcript Classifier Prototype

| Model | Parameters | Downloads | Likes | License |
|---|---|---|---|---|
| [google-bert/bert-base-uncased](https://hf.co/google-bert/bert-base-uncased) (classic baseline) | 110.1M | **3,239.3M** | **3,367** | Apache-2.0 |
| [distilbert/distilbert-base-uncased](https://hf.co/distilbert/distilbert-base-uncased) (fast/lighter) | 67.0M | 688.6M | 1,472 | Apache-2.0 |
| [FacebookAI/roberta-base](https://hf.co/FacebookAI/roberta-base) (stronger baseline) | 124.7M | 653.1M | 665 | MIT |

All three are English fill-mask encoders in the `transformers` library, fine-tuned on bookcorpus + Wikipedia. **Recommendation:** start with `bert-base-uncased` as the classic baseline; `distilbert-base-uncased` runs ~40% smaller/faster and `roberta-base` typically gains a point or two on classification accuracy — both make sensible bench partners for the earnings-transcript classifier prototype.

---

*Data sources: Yahoo Finance (AAPL profile, dividend & split actions), Google Maps (place lookup), Hugging Face Hub (model stats). Values are as returned at lookup time; verify before acting on them.*
