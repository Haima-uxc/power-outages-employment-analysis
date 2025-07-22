# power-outages-employment-analysis
Replication materials for "Lights Out, Jobs Gone: Uncovering The Hidden Toll Of Power Outages On Business"
# Lights Out, Jobs Gone: Uncovering The Hidden Toll Of Power Outages On Business

## Replication Materials

This repository contains replication materials for the paper "Lights Out, Jobs Gone: Uncovering The Hidden Toll Of Power Outages On Business" published in Energy Policy.

## Authors

- **Ruhaimatu Abudu** (North Dakota State University)
- **Ranjit Prasad Godavarthy** (North Dakota State University)  
- **Kwabena Dadson** (North Dakota State University)
- **Frank Selase Dzawu** (University of Nebraska, Lincoln)
- **Anastasia Ojong Maayuk-okpok** (Shanghai Maritime University)
- **Emmanuel Ato Kwamina Baidoo** (La Dade-Kotopon Municipal Assembly Department; Ghana Enterprises Agency)

## Abstract

Power outages impose substantial economic costs, yet causal evidence on employment effects remains limited. This study examines the causal impact of power outages on state-level employment in the United States using comprehensive data spanning 459 state-year observations from 2014-2022. We address endogeneity using weather events as instrumental variables, providing exogenous variation in outage exposure. Our analysis reveals a novel dual mechanism: outages simultaneously reduce employment through operational disruption (-2,380 jobs in year 1) while increasing it through reconstruction demand (+749 jobs immediately, +1,948 jobs in year 2), yielding a net positive effect of +318 jobs over three years. Regional heterogeneity analysis shows the West benefits substantially (+5,816 jobs/outage) while the South faces significant losses (-2,676 jobs/outage). Energy-intensive industries experience the largest negative impacts (-2,106 jobs/outage). These findings fundamentally challenge existing frameworks and provide crucial evidence for the $65 billion Infrastructure Investment and Jobs Act.

## Repository Structure

```
├── README.md                    # This file
├── data/                        # Data files
│   ├── raw/                     # Original data sources
│   ├── processed/              # Cleaned analysis datasets
│   └── data_dictionary.md      # Variable definitions
├── code/                       # Analysis scripts
│   ├── 01_data_cleaning.R      # Data preparation
│   ├── 02_descriptive_analysis.R # Summary statistics
│   ├── 03_main_regressions.R   # Main empirical analysis
│   ├── 04_robustness_checks.R  # Robustness tests
│   └── 05_tables_figures.R     # Output generation
├── output/                     # Results
│   ├── tables/                 # LaTeX tables
│   ├── figures/               # Figures and plots
│   └── results/               # Regression outputs
├── manuscript/                 # Paper files
│   ├── paper.tex              # Main LaTeX file
│   ├── references.bib         # Bibliography
│   └── paper.pdf              # Final manuscript
└── LICENSE                    # MIT License
```

## Data Sources

- **Employment Data**: Bureau of Labor Statistics Quarterly Census of Employment and Wages (QCEW)
- **Outage Data**: Compiled from utility reports and EIA-417 forms
- **Weather Data**: National Oceanic and Atmospheric Administration (NOAA)
- **Economic Controls**: Bureau of Economic Analysis, Federal Reserve Economic Data

## Key Findings

### Main Results
- **Dual Mechanism Identified**: Power outages create both job destruction and job creation
- **Temporal Pattern**: +749 jobs (immediate) → -2,380 jobs (year 1) → +1,948 jobs (year 2)
- **Net Effect**: +318 jobs over three years per major outage event

### Regional Heterogeneity
- **West Region**: +5,816 jobs per outage (reconstruction dominates)
- **South Region**: -2,676 jobs per outage (disruption dominates)
- **Policy Implication**: Target infrastructure investments to vulnerable regions

### Industry Effects
- **Energy-Intensive Industries**: -2,106 jobs per outage
- **Construction Sector**: Significant positive employment effects
- **Service Sector**: Mixed effects depending on outage duration

## Methodology

- **Identification Strategy**: Weather-based instrumental variables
- **Sample**: 51 jurisdictions (50 states + DC), 2014-2022
- **Estimation**: Panel fixed effects with state and year controls
- **Robustness**: COVID-19 controls, pre-pandemic subsample, alternative specifications

## Replication Instructions

### Software Requirements
- R version 4.0 or higher
- Required packages: `fixest`, `modelsummary`, `ggplot2`, `dplyr`, `stargazer`

### Running the Analysis
1. Clone this repository
2. Install required R packages
3. Run scripts in numerical order:
   ```r
   source("code/01_data_cleaning.R")
   source("code/02_descriptive_analysis.R")
   source("code/03_main_regressions.R")
   source("code/04_robustness_checks.R")
   source("code/05_tables_figures.R")
   ```

### Expected Runtime
- Data cleaning: ~5 minutes
- Main analysis: ~10 minutes
- Robustness checks: ~15 minutes
- Total: ~30 minutes on standard laptop

## Data Availability

Raw data files are compiled from publicly available government sources. Processed datasets used in the analysis are included in this repository. Original raw data can be obtained from:

- **BLS QCEW**: https://www.bls.gov/cew/
- **NOAA Weather**: https://www.noaa.gov/
- **EIA Energy**: https://www.eia.gov/

## Citation

If you use these materials, please cite:

```
Abudu, R., Godavarthy, R.P., Dadson, K., Dzawu, F.S., Maayuk-okpok, A.O., & Baidoo, E.A.K. (2025). 
Lights Out, Jobs Gone: Uncovering The Hidden Toll Of Power Outages On Business. 
Energy Policy, [Volume], [Pages].
```

## Policy Implications

Our findings directly inform infrastructure policy:

1. **Regional Targeting**: Prioritize grid investments in the South where disruption effects dominate
2. **Best Practices**: Study Western states' successful conversion of outages into economic opportunities
3. **Industry Focus**: Develop specialized support for energy-intensive industries
4. **Recovery Planning**: Design reconstruction programs with 18-24 month activation timelines

## Contact

**Corresponding Author:** Ruhaimatu Abudu  
**Email:** ruhaimatu.abudu@ndsu.edu  
**Affiliation:** North Dakota State University, Department of Economics

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

We thank seminar participants and conference attendees for helpful comments. Any errors are our own.

---

**Keywords:** Power outages, Employment effects, Infrastructure policy, Regional heterogeneity, Instrumental variables
