
# Measuring the Individual-Level Precision of Implicit Measures

This repository contains all code, data, and documentation for the study examining the **individual-level precision** of six widely used implicit measures: IAT, BIAT, ST-IAT, AMP, EPT, and GNAT. The focus is on the width of bootstrapped confidence intervals around individual scores, used as a measure of precision.

In general, results should be viewable in the corresponding .html files associated with each analysis file. If desiring to run the code from scratch, move all files out from the "processed" directory, as otherwise these will be automatically loaded (rather than recomputing from scratch). Run all processing files in numeric order (i.e., 01, then 02, then 03) and then follow a similar approach for the analysis files.  

---

### 📁 Directory Structure

```
├── data/
│   ├── raw/                    # Raw data files as received from original sources
│   ├── processed/              # Cleaned, trial-level data ready for analysis
│   └── results/                # Score-level outputs, summaries, and CI width results
│
├── code/
│   ├── processing/             # Scripts that prepare and score the data for analysis
│   │   ├── 01_processing.Rmd              # Main score processing (used in manuscript)
│   │   ├── 02_processing_native.Rmd       # Processing for native task scores (Supplementary Materials)
│   │   ├── 03_processing_explicit.Rmd       # Processing for the explicit measures (Supplementary Materials)
│   │
│   ├── analysis/               # R Markdown files and outputs for statistical analysis
│   │   ├── 01_analysis.Rmd                  # Main analyses reported in the manuscript
│   │   ├── 01_analysis.html
│   │   ├── 02_analysis_native.Rmd          # Analyses of native scores (Supplementary Materials)
│   │   ├── 02_analysis_native.html
│   │   ├── 03_analysis_preregistered.Rmd   # Original preregistered analyses
│   │   ├── 03_analysis_preregistered.html
│   │   ├── 04_analysis_explicit.Rmd   # Analyses for the precision of the explicit measures (Supplementary Materials)
│   │   ├── 04_analysis_explicit.html
│   │   ├── D score categories and intervals.xlsx  # CI-based category cutoffs
│   │   ├── models/                       # Pre-saved model objects used in RQ1–RQ3
│   │   │   ├── fit_beta_ci_width_proportions.rds
│   │   │   ├── fit_beta_diff_zero.rds
│   │   │   ├── fit_beta_discriminability.rds
│   │   ├── plots/                        # Figures for manuscript and supplements
│   │   │   ├── figure_2_cis_by_domain.pdf
│   │   │   ├── figure_3_metaanalyses.pdf
│   │   │   ├── figure_s1_cis_by_domain.pdf
│   │   │   ├── figure_s2_metaanalyses.pdf
│
├── manuscript/                # Final manuscript and figure files
│
├── preregistration/
│   ├── preregistration.docx              # Original preregistration
│   ├── deviations.docx                   # Documentation of deviations from preregistration
│   └── analyses using preregistered code/  # Supporting files for preregistered analysis
│
├── README.md                  # This file
```

---

### 🧭 How to Reproduce the Analysis

1. **Process and score the data**
   - Run `01_processing.Rmd` to prepare the main dataset.
   - Optionally, run `02_processing_native.Rmd` for native-score versions used in the Supplementary Materials, and run `03_processing_explicit.Rmd` for explicit measures used in the Supplementary Materials.

2. **Run the analyses**
   - `01_analysis.Rmd`: Main manuscript analyses
   - `02_analysis_native.Rmd`: Supplementary analyses using native scores
   - `03_analysis_preregistered.Rmd`: Original preregistered analyses (not used in final manuscript)
   - `04_analysis_explicit.Rmd`: Supplementary analyses using explicit measures

3. **Figures**
   - Final plots used in the manuscript are saved in `code/analysis/plots/`.

4. **Model outputs**
   - Final model objects used to generate all reported statistics are saved in `code/analysis/models/`.

---

### 📦 Dependencies

Specified in the corresponding .Rmd files.

### ❓ Questions

For questions about reproducing the analyses or reusing the data/code, please contact:  
**jamie.cummins@unibe.ch** or **ian.hussey@unibe.ch**.
