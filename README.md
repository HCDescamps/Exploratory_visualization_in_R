# Exploratory Visualization in R: Mtcars Dataset

## Overview

This project demonstrates an exploratory data analysis workflow in **R** using the classic `mtcars` dataset. The objective is to explore relationships between vehicle characteristics and fuel efficiency through visualization, dimensionality reduction, and statistical modeling.

The analysis is implemented as a reproducible **Quarto** notebook and managed using **renv** for package reproducibility.

---

## Research Questions

This analysis explores:

1. How do vehicle characteristics relate to fuel efficiency?
2. Which variables contribute most to variation across vehicles?
3. How does vehicle weight influence miles per gallon?
4. How do horsepower and other mechanical characteristics affect fuel efficiency?
5. Can fuel efficiency be predicted using vehicle properties?

---

## Analysis Workflow

The Quarto notebook includes:

### 1. Data exploration

- Dataset overview
- Summary statistics
- Variable inspection
- Basic visualization of vehicle characteristics

### 2. Principal Component Analysis (PCA)

PCA is used to:

- Reduce dimensionality
- Identify major sources of variation
- Determine which vehicle features contribute most strongly to variation

Outputs include:

- Variance explained by principal components
- PCA loadings
- PCA score visualization
- PCA biplot

### 3. Correlation and visualization analysis

Relationships between:

- Weight (`wt`)
- Horsepower (`hp`)
- Displacement (`disp`)
- Miles per gallon (`mpg`)

are explored using graphical and statistical approaches.

### 4. Statistical modeling

Linear regression models are used to investigate predictors of fuel efficiency:

```r
mpg ~ wt + hp
```

Model diagnostics are performed to assess:

- Residual behavior
- Model assumptions
- Fit quality

---

## Repository Structure

```
.
├── _quarto.yml                 # Quarto project configuration
├── README.md                   # Project documentation
├── renv.lock                   # Reproducible R environment
│
├── notebooks/
│   └── 01_exploration.qmd      # Main exploratory analysis
│
├── scripts/                    # Supporting R scripts
│
├── results/                    # Generated outputs and figures
│
└── renv/                       # Package environment management
```

---

## Software Requirements

- R (>= 4.6)
- Quarto
- R packages managed through `renv`

Main packages:

- tidyverse
- ggplot2
- dplyr
- ggpubr
- smplot2
- factoextra

---

## Reproducibility

This project uses `renv` to ensure that package versions are reproducible.

To reproduce the analysis:

1. Clone the repository

```bash
git clone <repository-url>
cd Exploratory_visualization_in_R
```

2. Restore the R environment

```r
renv::restore()
```

3. Render the Quarto notebook

```bash
quarto render
```

The HTML report will be generated from the `.qmd` source file.

---

## Key Findings

The exploratory analysis shows that:

- Vehicle weight is strongly associated with reduced fuel efficiency.
- Horsepower and displacement are major contributors to vehicle variation.
- Principal component analysis captures most of the variance using a small number of components.
- A combination of weight and horsepower provides a strong explanation of fuel efficiency differences between vehicles.

