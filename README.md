# The Impact of Regional Trade Agreements on Trade Flows: The Case of ECOWAS and COMESA

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![R](https://img.shields.io/badge/R-4.0+-blue.svg)](https://www.r-project.org/)

A comprehensive econometric analysis using gravity models to examine the impact of regional trade agreements (ECOWAS and COMESA) on bilateral trade flows in Sub-Saharan Africa.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Methodology](#methodology)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Citation](#citation)

## Project Overview

This repository contains the complete analysis for my MSc thesis on regional trade agreements in Sub-Saharan Africa. The study employs gravity models to investigate how membership in COMESA and ECOWAS influences bilateral trade flows, controlling for various economic and geographic factors.

### Key Research Questions

- How do regional trade agreements affect bilateral trade flows?
- What is the relative impact of COMESA vs ECOWAS membership?
- How do economic size, distance, and other gravity variables influence trade?

## Data Sources

- **World Development Indicators (WDI)**: GDP, population, and economic indicators
- **Gravity Dataset**: Bilateral trade flows, distances, and geographic variables
- **Regional Trade Agreement Membership**: COMESA and ECOWAS membership data
- **Regional Analysis**: Country-specific data for COMESA and ECOWAS member states

## Methodology

The analysis employs several econometric approaches:

- **Ordinary Least Squares (OLS)** regression
- **Generalized Method of Moments (GMM)** estimation
- **Panel data analysis** with fixed and random effects
- **Robustness checks** and diagnostic tests

## Project Structure

```
msc_thesis_analysis/
├── src/                          # Source code
│   ├── data/                     # Data processing scripts
│   │   ├── dataset_creator.r     # Main dataset construction
│   │   ├── data_exploration.r    # Exploratory data analysis
│   │   └── world_development_indicators.r
│   ├── features/                 # Feature engineering
│   │   ├── comesa_description.r  # COMESA-specific analysis
│   │   ├── ecowas_description.r  # ECOWAS-specific analysis
│   │   └── global_description.r  # Global trade patterns
│   ├── models/                   # Modeling scripts
│   │   ├── model_estimation.r    # Main gravity model estimation
│   │   ├── regressions.r         # Regression analysis
│   │   ├── gmm_analysis.r        # GMM estimation
│   │   ├── panel_tests.r         # Panel data diagnostics
│   │   └── ols_test.r            # OLS robustness tests
│   └── visualization/            # Visualization scripts
│       └── major_trade_partners.r
├── reports/                      # Analysis reports and results
│   ├── figures/                  # Generated figures and plots
│   ├── predicted_vs_actual.r     # Model validation
│   ├── comparative_tables.r      # Results comparison
│   ├── descriptives.r            # Descriptive statistics
│   └── regression_diagnostics.r  # Model diagnostics
├── docs/                         # Documentation
│   └── regional_trade_agreements_thesis.pdf
├── data/                         # Data directory (not tracked)
├── models/                       # Trained models (not tracked)
├── results/                      # Analysis results (not tracked)
├── .gitignore                    # Git ignore rules
├── LICENSE                       # MIT License
└── README.md                     # This file
```

## Installation

### Prerequisites

- R version 4.0 or higher
- Required R packages: `tidyverse`, `plm`, `stargazer`, `ggplot2`, `haven`

### Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/regional-trade-agreements-ecowas-comesa.git
   cd regional-trade-agreements-ecowas-comesa
   ```
2. Install required packages:

   ```r
   # Install required packages
   install.packages(c("tidyverse", "plm", "stargazer", "ggplot2", "haven",
                      "lmtest", "sandwich", "multiwayvcov", "clubSandwich"))
   ```

## Usage

### Data Preparation

Run the data preparation scripts in order:

```r
# 1. Create main dataset
source("src/data/dataset_creator.r")

# 2. Explore data
source("src/data/data_exploration.r")

# 3. Process regional indicators
source("src/data/world_development_indicators.r")
```

### Model Estimation

Execute the main analysis:

```r
# Run gravity model estimation
source("src/models/model_estimation.r")

# Run regression analysis
source("src/models/regressions.r")
```

### Generate Results

Create tables and figures:

```r
# Generate comparative tables
source("reports/comparative_tables.r")

# Create diagnostic plots
source("reports/regression_diagnostics.r")
```

## Results

### Key Findings

- Regional trade agreements significantly increase bilateral trade flows
- COMESA shows stronger trade creation effects than ECOWAS
- Economic size and geographic distance remain dominant gravity variables
- Results are robust across different estimation methods

### Model Performance

- OLS: R² = 0.78, F-statistic significant at 1% level
- GMM: Hansen J-test p-value = 0.24 (instrument validity confirmed)
- Panel models: Hausman test favors random effects specification

## Contributing

This is an academic thesis repository. For questions or collaboration opportunities, please contact the author.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation

If you use this code or analysis in your research, please cite:

```
Osei-Owusu, A. K. (2017). *The impact of regional trade agreements on trade flows: The case of ECOWAS and COMESA* [Master's thesis].
```

## 📞 Contact

**Author**: Albert Kwame Osei-Owusu
**Email**: `ako@riitas-consult.org`

---

*This repository follows the cookiecutter data science project structure for reproducibility and best practices.*
