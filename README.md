# R for eaRth: Data Visualisation and Exploration Challenge at UseR!2026 🌍

An data challenge accompanying the [useR!2026](http://user2026.r-project.org/) conference, aimed at improving the precision of methane emission estimation based on spectral data from the **Sentinel-2** satellite.

The organizers posit that current statistical models have reached an algorithmic optimization threshold; further progress requires a process of *knowledge exploration* and understanding **why** models fail under specific geographic and temporal conditions.

---

## 🎯 Research Tracks

Participants may focus on one of the following three tracks:

### Track 1 — Feature Engineering & Denoising
Search a set of 198 spectral indices for non-linear interactions that most effectively denoise the signal and isolate actual methane emissions from ground-level interference.

### Track 2 — Seasonal Bias
Explain why the baseline model shows unnaturally high precision in certain months (e.g., May: MAE 18.5, Pearson 0.62) while the error is significantly higher in others (e.g., April: MAE 40.5). Possible factors include vegetation states, solar angles, and ground humidity.

### Track 3 — Regional Calibration
Adapt the model to local albedo. The greatest challenge is the Middle East (MAE 36.05) — the model must work as effectively on bright sands as it does in the dark forests of Europe.

---

## 📊 Dataset

| Element | Description |
|---|---|
| **Source** | Sentinel-2 (2024), data provided by SRON (Netherlands Institute for Space Research) |
| **Target variable** | `methane_rate` — methane emission intensity in t/h |
| **Input features** | 198 spectral indices (NDVI, EVI, LAI, NDWI, MNDWI, SWIR…) computed with the `spyndex` library |
| **Structure** | 439 unique measurement series, 5 folds for cross-validation |
| **Baseline** | MAE 29.47; Pearson 0.24 |

---

## 📦 Submission Requirements

1. **Poster** — an A0 poster as a single PDF file (in the horizontal orientation) summarizing the obtained results, demonstrating the physical soundness of the model and the most important factors influencing the prediction.
2. **Source code** — in R, Python, or any other programming language, allowing for full reproduction of the analysis and visualization.
3. **Author data** — name, surname, and contact information (one submitter for group entries).
4. **License** — original and previously unpublished work, released under **CC BY-SA**.

Total submission size (including attachments): **max. 10 MB**.

---

## 📅 Deadline

**June 30, 2026, 23:59 PDT (UTC-7)**

---

## 🏆 Prizes and Announcement

- The best submissions will be presented during a **dedicated session at the useR!2026 conference**.
- The top entries will receive **prizes**.

---

## 🔎 Evaluation Criteria

Each submission is evaluated by a three-person expert panel (Remote Sensing specialist, data analyst, and an external expert from ESA), scored **0–10 points** in three categories:

- **Relevance to the research question** — did the participant explain the causes of low R² in difficult months or regions?
- **Visual simplicity vs. data richness** — does the visualization show error distribution and correlation with actual emissions?
- **Narrative power** — does the data story clearly explain why the proposed model is scientifically more reliable?

### Technical metrics (auxiliary)

- **Weighted MAE** — error reduction specifically for high-emission events
- **R² Improvement** — increased ability of the model to explain data variance in challenging regions
- **Stability Score** — consistency of results (R² and MAE) across continents and seasons

---

## 📬 Contact and Submissions

Submissions should be sent as separate emails to: user2026warsaw@gmail.com
Titled "R for eaRth"

---

*Organized as part of the useR! 2026 conference.*
