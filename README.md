# Heart Failure Clinical Records Synthetic Data Project

[![Quarto Report](https://img.shields.io/badge/Quarto-Published-brightgreen)](https://linuschirchir.quarto.pub/heart-failure-clinical-records-synthetic-data-project/)

This project explores **synthetic data generation and quality assessment** using the [Heart Failure Clinical Records dataset](https://archive.ics.uci.edu/dataset/519/heart+failure+clinical+records).  
The aim is to evaluate how well different synthetic data methods preserve the utility and privacy of the original dataset, while ensuring safe data use for research.

---

## 📑 Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Site Structure](#site-structure)
- [Methods & Workflow](#methods--workflow)
- [Customisation](#customisation)
- [Running Locally](#running-locally)
- [References](#references)
- [Author](#author)
- [License](#license)

---

## 🔎 Introduction
This project investigates synthetic data methods (MICE, CART, Synthpop, Metadata-based) applied to the Heart Failure Clinical Records dataset.  
It evaluates **utility, fidelity, and privacy** of synthetic datasets using statistical and ML-based metrics.  

---

## 🛠️ Prerequisites
- **R (≥4.0)**  
- **Quarto**  
- R packages: `tidyverse`, `mice`, `synthpop`, `caret`, `xgboost`, `psych`, `GGally`, `corrplot`, `VIM`, `FNN`, `infotheo`, `transport`, `patchwork`

---

## ⚙️ Installation
Clone this repository:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
````

Install the required R packages:

```r
install.packages(c(
  "tidyverse", "mice", "synthpop", "caret", "xgboost", "psych",
  "GGally", "corrplot", "VIM", "FNN", "infotheo", "transport", "patchwork"
))
```

---

## 📂 Site Structure

```
├── _freeze/                                     # Quarto cache (auto-generated, ignored in Git)
├── _publish.yml                                 # Quarto publishing configuration
├── _quarto.yml                                  # Quarto project configuration
├── .gitignore                                   # Files and folders excluded from Git tracking
├── .Rhistory                                    # R console history (should be gitignored)
├── data/                                        # Data folder (real and synthetic datasets)
├── styles/                                      # Custom CSS for report styling
├── heart_failure_synthetic_data_project.qmd     # Main Quarto analysis document
├── heart_failure_synthetic_data_project.html    # Rendered HTML report
├── heart_failure_synthetic_data_project.docx    # Exported Word document
├── heart_failure_synthetic_data_project.tex     # Exported LaTeX document
├── heart_failure_synthetic_data_project_files/  # Quarto-generated assets (figures, libs)
├── heart_failure_synthetic_data_project.Rproj   # RStudio project file
├── heart_failure_synthetic_data_project.log     # Rendering log
```

---

## 🔬 Methods & Workflow

1. **Data Imputation & Synthesis**

   * Parametric (MICE), CART, Synthpop, Metadata-driven

2. **Quality Assessment**

   * Utility: Accuracy, pMSE, AUC
   * Fidelity: Histogram Similarity, Correlation, Mutual Information
   * Privacy: Replication checks, Neighbors’ Privacy Score, Membership Inference

3. **Visualisation & Reporting**

   * Missingness maps, correlation heatmaps, comparative plots

---

## 🎨 Customisation

* Modify **`_quarto.yml`** for theme, format, and publishing settings
* Adjust **`styles/`** for custom CSS styling
* Replace datasets inside **`data/`** to run the workflow on other clinical datasets

---

## 🚀 Running Locally

Render the Quarto report:

```bash
quarto render heart_failure_synthetic_data_project.qmd --to html
```

Or preview live in your browser:

```bash
quarto preview heart_failure_synthetic_data_project.qmd
```

---

## 📚 References

* UCI Machine Learning Repository: [Heart Failure Clinical Records Dataset](https://archive.ics.uci.edu/dataset/519/heart+failure+clinical+records)
* Nowok, B., Raab, G., & Dibben, C. (2016). *synthpop: Bespoke Creation of Synthetic Data in R*
* van Buuren, S., & Groothuis-Oudshoorn, K. (2011). *mice: Multivariate Imputation by Chained Equations in R*

---

## 👨‍💻 Author

**Linus Chirchir**
🌐 [Website](https://linuschirchir.com)
💼 [LinkedIn](https://linkedin.com/in/linuschirchir)

---

## 📜 License

This project is licensed under the MIT License. You are free to use, modify, and distribute it as long as proper attribution is provided. See the `LICENSE` file for more information.

---
