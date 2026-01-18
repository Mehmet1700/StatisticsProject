# Determinants of GDP per Capita Growth in the EU

A panel data analysis examining the effects of migration, unemployment, and investment on economic growth across EU-27 member states (2014–2023).

## 📊 Project Overview

This project analyzes the determinants of GDP per capita growth in the European Union using panel data econometrics. The analysis includes:

- **Pooled OLS**, **Fixed Effects**, and **Random Effects** models
- Diagnostic tests (Hausman, heteroskedasticity, serial correlation)
- Robust standard errors (cluster-robust and Newey-West)
- Visualizations and academic poster

## 📁 Project Structure

```
StatisticsProject/
├── README.md
└── src/
    ├── analysis_eu_growth.Rmd    # Main analysis (R Markdown)
    ├── analysis_eu_growth.html   # Rendered analysis report
    ├── poster_eu_growth.rmd      # Academic poster
    ├── poster_eu_growth.html     # Rendered poster
    ├── poster.css                # Poster styling
    ├── references.bib            # Bibliography
    ├── apa.csl                   # Citation style
    └── rds/                      # Exported data & models
        ├── panel_data.rds
        ├── fe_model.rds
        └── re_model.rds
```

## 🚀 Quick Start

### Prerequisites

- R (≥ 4.0)
- RStudio (recommended) or VS Code with R extension
- Required R packages:

```r
install.packages(c(
  "eurostat", "tidyverse", "plm", "lmtest", "sandwich",
  "stargazer", "corrplot", "kableExtra", "scales", "moments"
))
```

### Render Analysis

```bash
cd src
Rscript -e "rmarkdown::render('analysis_eu_growth.Rmd')"
```

### Render Poster

```bash
cd src
Rscript -e "rmarkdown::render('poster_eu_growth.rmd')"
```

## 👀 View Output

### Open Analysis Report

```bash
open src/analysis_eu_growth.html
```

### Open Academic Poster

```bash
open src/poster_eu_growth.html
```

> **Windows:** Replace `open` with `start`  
> **Linux:** Replace `open` with `xdg-open`

## 📈 Data Sources

All data retrieved from [Eurostat](https://ec.europa.eu/eurostat/data/database):

| Variable | Eurostat Code | Description |
|----------|---------------|-------------|
| GDP per capita | `sdg_08_10` | Real GDP per capita in PPS |
| Net Migration | `migr_netmigr` | Net migration (immigration - emigration) |
| Population | `demo_gind` | Total population |
| Unemployment | `une_rt_a` | Unemployment rate (% of active population) |
| Investment | `sdg_08_11` | Gross fixed capital formation (% of GDP) |

## 📐 Methodology

- **Panel Data:** EU-27 countries, 2014–2023 (~270 observations)
- **Models:** Pooled OLS, Fixed Effects (within), Random Effects
- **Model Selection:** Hausman test, F-test, Breusch-Pagan LM test
- **Robust Inference:** Cluster-robust SE (HC1), Newey-West HAC

## 📄 License

This project is for academic purposes.

## 👥 Authors

- Mehmet, Alexander, Ammar, Khuzaima