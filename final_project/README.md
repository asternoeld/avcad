# From a Crop's Environmental Fingerprint to Global Yield Trends
### AVCAD final project (2372 — Analysis and Visualization of Complex Agro-Environmental Data), GreenDS MSc, ISA/ULisboa 2025/2026

**Authors:** Aster Noel Dsouza (29211) · David Heleno Bebiano da Costa Morais (29400)

A coherent exploratory, inferential and multivariate analysis of Smart-Farming agro-environmental
data, spanning the individual plot to the planet. Companion project to our Applied Machine Learning
(2373) study — same theme and data, independent analyses.

## What's inside
| Path | Contents |
|------|----------|
| `report/` | Written report (`.docx` and `.pdf`) — the main deliverable (5 chapters + annex) |
| `notebook/` | `AVCAD_final_project_code_annex.ipynb` — reproduces every figure & statistic (Colab-ready) |
| `dashboard/` | `AVCAD_dashboard.html` — interactive Plotly dashboard (open in any browser) |
| `data/` | The three datasets |
| `figures/` | All 13 report figures (PNG) |
| `AI_USAGE.md` | AI-usage declaration with prompts |
| `requirements.txt` | Python dependencies |

## The three datasets
1. **Crop Recommendation** (Kaggle, 2,200×7, 22 crops) — core multivariate analysis.
2. **OECD/FAO crop production** (48 countries, 1990–2025, 4 crops) — real geographical & temporal trends.
3. **Crop Yield** (Kaggle, synthetic) — supporting categorical hypothesis tests.

## How to reproduce
```bash
pip install -r requirements.txt
jupyter notebook notebook/AVCAD_final_project_code_annex.ipynb   # or open in Google Colab
```
Place the three CSVs from `data/` next to the notebook (or in a `data/` subfolder).

## Headline findings
- Crop groups occupy **statistically distinct** soil–climate envelopes (ANOVA/Kruskal p < 0.001 for every variable; humidity, nitrogen and rainfall separate them most).
- The environmental space is **multidimensional** (3 PCs for 60% variance); **LDA** separates groups at **85%** accuracy; "cereals" is the least coherent group (rice ≠ maize environmentally).
- **Clustering** only partly matches botanical groups — environmental niche cuts across taxonomy.
- In the **synthetic** yield data only management variables (irrigation/fertiliser) carry signal — a clean external-validity caution.
- **Real** OECD yields rose significantly 1990–2025 (maize +0.77 t/ha per decade) with a significant geographical gap (Oceania/Americas high, Africa low).

## Relationship to the ML (2373) project
Same datasets and Smart-Farming theme; analyses are independent. ML = supervised prediction
(classification/regression, SHAP, climate stress-test). AVCAD = descriptive/inferential/unsupervised
(EDA, hypothesis tests, PCA/LDA/clustering, geo-temporal visualisation). No ML model is reused here.
