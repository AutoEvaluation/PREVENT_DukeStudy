# Real World Performance of PREVENT Cardiovascular Risk Equations Using Duke Electronic Health Records

This repository contains the analysis code used in the study:

> **Real World Performance of PREVENT Cardiovascular Risk Equations Using Duke Electronic Health Records**

## Key Research Question
Does the PREVENT Equations model maintain strong 5-year cardiovascular disease (CVD) risk prediction performance **across demographic and socioeconomic subgroups** under **real-world EHR conditions**, including when laboratory or vital signs data are missing?

## Key Findings
- **Discrimination**: PREVENT demonstrated **strong and consistent discrimination** across patient subgroups.
- **Calibration**: The original PREVENT model modestly **underestimated risk** (overall calibration ratio ~0.89), with greater underestimation in Black patients and patients from the highest area deprivation index (ADI) quartile.
- **Local Model Adaptation**: Re-estimating coefficients using the local EHR cohort **improved calibration only slightly** and did **not improve discrimination**.
- **Missing Data**: PREVENT performance remained stable when **relevant imputation methods** were applied, indicating suitability for clinical environments where some measurements may be unavailable.

**Meaning:** PREVENT can be effectively applied in routine clinical settings, including those with incomplete EHR data, to detect elevated CVD risk.

---

## Data Access Notice
This repository **does not include Duke EHR data** or trained model objects, in accordance with DUHS data use and privacy regulations.  
All results and visualizations in this codebase correspond to the manuscript and supplementary materials.  
Plots and tables visible in this repository are limited placeholders; **final figures are included in the submitted manuscript**.

---

## Repository Structure
```
code/
│
├── EDA_plots/
│   ├── EDA.Rmd
│   ├── calibration_across_models_plots.Rmd
│   ├── calibration_across_cohorts_plots.Rmd
│   ├── cindex_across_model_bootstrap.Rmd
│   ├── cindex_difference_adi_stratified.Rmd
│   ├── hazard_ratio.Rmd
│   └── radar_plots.Rmd
│
├── calibration/
│   ├── cal_exp3.Rmd
│   └── calibration_ratio.Rmd
│
├── cohort_development/
│   ├── relax_cohort_dnn_model.ipynb
│   ├── relax_cohort_race_sex_imputation.ipynb
│   ├── strict_cohort.Rmd
│   └── strict_cohort_dnn_model.ipynb
│
├── discrimination/
│   ├── cindex_across_cohorts.Rmd
│   ├── cindex_across_models.Rmd
│   ├── cindex_across_models_bootstrap.Rmd
│   ├── cindex_exp3.Rmd
│   ├── cindex_prevent_adi_stratified.Rmd
│   └── cindex_sdoh_difference.Rmd
│
└── data/
    └── (placeholder — no EHR data included)
```
