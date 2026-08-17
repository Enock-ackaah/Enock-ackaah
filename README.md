# Enock Kumi Ackaah

### Applied Statistics | Machine Learning | Biomedical Data Science | Reliable AI

I am an applied statistician and biomedical data-science researcher focused on developing reliable, interpretable, and reproducible statistical and machine-learning methods for high-dimensional and multimodal biomedical data.

I am currently pursuing an **M.S. in Applied Statistics with a concentration in Machine Learning and Data Science at Georgia State University**. I previously earned an **M.S. in Statistics from The University of Akron**, where I served as a Graduate Teaching Assistant and conducted research in machine learning, survival analysis, cancer prediction, and high-dimensional biomedical data.

My long-term research goal is to develop **human-supervised explainable AI methods and statistical reliability-auditing frameworks for high-dimensional, small-sample, and multimodal cancer-prediction models**.

---

## Research Focus

- Reliable and explainable artificial intelligence for cancer prediction
- Statistical reliability of high-dimensional and small-sample models
- Survival prediction using clinical and molecular data
- Multimodal integration of clinical and transcriptomic information
- RNA-sequencing and DNA-methylation analysis
- Feature-selection stability and explanation reproducibility
- Model calibration, uncertainty quantification, and external validation
- Repeated and nested cross-validation for biomedical prediction
- Human-supervised AI for healthcare decision support
- Reproducible biomedical machine learning

---

## Current Research

### TCGA-KIRC Clinical and RNA-seq Survival Prediction

I recently completed a reproducible survival-prediction study using **TCGA Kidney Renal Clear Cell Carcinoma (TCGA-KIRC)** data to evaluate whether high-dimensional RNA-seq information improves progression-free interval prediction beyond clinical predictors.

The study compared:

1. Clinical-only Cox proportional hazards models
2. RNA-only penalized Cox models
3. Integrated Clinical + RNA multimodal penalized Cox models

The analysis included:

- 529 PFI-eligible patients
- 159 progression events
- Protein-coding RNA-seq features
- Training-fold-specific RNA preprocessing and feature selection
- Repeated nested cross-validation
- 10 repeats × 5 outer folds
- 50 held-out evaluations per model
- Time-dependent AUC at 1, 3, and 5 years
- Brier score and integrated Brier score
- Kaplan-Meier risk stratification
- Calibration analysis
- Repeated feature-selection stability
- Pairwise Jaccard similarity
- RNA feature-count sensitivity analysis

### Main Findings

| Model | Mean Repeated C-index |
|---|---:|
| Clinical | **0.8120** |
| RNA | 0.7173 |
| Clinical + RNA | 0.7989 |

The clinical-only model achieved the strongest overall discrimination.

The mean paired difference between Clinical + RNA and Clinical was:

`-0.0131`

with a repeat-level 95% bootstrap confidence interval of approximately:

`[-0.0188, -0.0062]`

Additional findings included:

- Clinical-only models had the highest time-dependent AUC at 1, 3, and 5 years
- Clinical-only models had the lowest Brier scores and integrated Brier score
- Clinical-only models showed the best overall calibration
- Clinical + RNA models produced the strongest Kaplan-Meier risk-group separation
- 148 unique RNA genes were selected across 50 multimodal fits
- Mean pairwise Jaccard similarity was 0.3251
- Six RNA genes were selected in at least 40 of 50 models
- Multimodal C-index remained approximately 0.798 across 100, 250, and 500 retained RNA features

Frequently selected genes included:

- SLC10A2
- CXCL5
- CLTRN
- SLC6A19
- SCIN
- NDNF
- G6PC
- FABP7
- PRAME
- CAPN6

The study demonstrates that adding high-dimensional transcriptomic information does not necessarily improve out-of-sample survival prediction beyond a parsimonious clinical model, even when multimodal models achieve strong risk stratification.

[View repository](https://github.com/Enock-ackaah/TCGA-KIRC-PFI-Multimodal-Survival)

---

### Statistical Reliability of High-Dimensional Breast Cancer RNA-Sequencing Models

I am studying how development sample size affects predictive performance, feature-selection stability, coefficient-direction reproducibility, probability accuracy, and external generalization in machine-learning models for estrogen-receptor status prediction.

The study uses:

- GSE81538 as the development cohort
- GSE96058 as the independent external-validation cohort
- 18,213 aligned RNA-sequencing features
- 397 development tumors
- 405 sensitivity-analysis tumors
- 3,073 external-validation tumors
- Repeated stratified validation
- Development-sample-size stress testing
- Feature-selection stability analysis
- Coefficient-direction reproducibility analysis
- Bootstrap confidence intervals
- External validation
- Brier-score assessment
- Clean-environment model reproducibility verification

Key results include:

- External AUROC: **0.9699**
- 95% CI: **0.9597–0.9788**
- Balanced accuracy: **0.9390**
- Sensitivity-model AUROC: **0.9672**
- Sensitivity-model Brier score: **0.0510**
- Mean Jaccard similarity reached **0.7693**
- Severe instability was observed at very small development sample sizes

The project includes reproducible notebooks, compact results, a reusable fitted model, model documentation, SHA-256 artifact verification, and archived research software.

[View repository](https://github.com/Enock-ackaah/statistical-reliability-high-dimensional-er-models)

**Software:**  
Ackaah, E. K. (2026). *Statistical Reliability of High-Dimensional ER-Status Prediction Models* (Version 0.1.1). Zenodo.  
DOI: `10.5281/zenodo.21524693`

---

## Publications and Research Software

### Cancer Classification in Low- and High-Dimensional Biomedical Data Using Machine Learning Models

**Ackaah, E. K., & Datta, S. (2026).**

Preprint examining supervised machine-learning performance in low-dimensional breast-tissue data and extremely high-dimensional osteosarcoma DNA-methylation data.

The study compared:

- Logistic Regression
- Support Vector Machines
- Random Forest
- K-Nearest Neighbors
- Principal Component Analysis for high-dimensional reduction

The work highlights the reliability challenges that arise when dimensionality is extremely high relative to sample size.

Preprint DOI:

`10.20944/preprints202608.0073.v1`

[View repository](https://github.com/Enock-ackaah/cancer-classification-low-high-dimensional-data)

---

### Artificial Intelligence in the Biomedical Sciences and Healthcare

Co-authored narrative review with Professor Sujay Datta examining the impact, benefits, limitations, and implementation challenges of artificial intelligence in biomedical science and healthcare.

Topics include:

- Machine learning
- Deep learning
- Multimodal AI
- Drug discovery
- Clinical decision support
- Human-AI collaboration
- Reproducibility
- Explainability
- Bias and fairness
- Data leakage
- Privacy and governance
- Prospective monitoring

The review emphasizes transparent reporting, clinically meaningful evaluation, human oversight, and reliability-centered AI development.

---

### Frozen 72-CpG DNA Methylation Classifier for Colorectal Tumor Detection

Archived reproducible machine-learning software for colorectal tumor classification using a fixed DNA-methylation signature.

**Software:**  
Ackaah, E. K. (2026). *Frozen 72-CpG DNA Methylation Classifier for Colorectal Tumor Detection* (Version 1.0.0). Zenodo.

DOI:

`10.5281/zenodo.21819138`

---

## Selected Research Projects

### DNA-Methylation-Based Tumor-Normal Classification

Interpretable tumor-versus-normal classification using LASSO and Elastic Net logistic regression with high-dimensional DNA-methylation data.

[View repository](https://github.com/Enock-ackaah/DNA-Methylation-Based-Tumor-Normal-Classification)

---

### Transcriptomic Comparison of CHP and IPF

Comparative transcriptomic analysis of GSE150910 using RNA-sequencing data and DESeq2.

[View repository](https://github.com/Enock-ackaah/Transcriptomic-Comparison-of-Chronic-Hypersensitivity-Pneumonitis-and-Idiopathic-Pulmonary-Fibrosis-)

---

### Promoter Prediction Using k-mers

Machine-learning promoter prediction using k-mer sequence encoding and Random Forest classification.

[View repository](https://github.com/Enock-ackaah/promoter-prediction-using-kmers)

---

### Lung Cancer Machine-Learning Presentation

Graduate presentation examining machine-learning methods and validation considerations for lung-cancer prediction.

[View repository](https://github.com/Enock-ackaah/lung-cancer-ml-presentation)

---

## Technical Skills

### Programming and Research Computing

- Python
- R
- SQL
- C++
- Git
- GitHub
- Jupyter Notebook / JupyterLab
- Visual Studio Code

### Machine Learning

- Logistic and multinomial regression
- Support Vector Machines
- Random Forest
- K-Nearest Neighbors
- LASSO
- Elastic Net
- Principal Component Analysis
- Penalized Cox regression
- Feature selection
- High-dimensional predictive modeling

### Validation and Reliability

- Repeated cross-validation
- Nested cross-validation
- Bootstrap confidence intervals
- External validation
- Time-dependent AUC
- Calibration analysis
- Brier score
- Integrated Brier score
- Kaplan-Meier risk stratification
- Feature-selection stability
- Jaccard similarity analysis
- Sensitivity analysis
- Reproducibility auditing

### Statistical Methods

- Linear models
- Logistic regression
- Survival analysis
- Cox proportional-hazards regression
- Bayesian statistics
- Multivariate analysis
- Nonparametric methods
- Experimental design
- Permutation tests

### Biomedical Data Science

- RNA sequencing
- DNA methylation
- High-dimensional omics
- Clinical + molecular multimodal data
- TCGA
- GEO
- Cancer classification
- Survival prediction
- Transcriptomic modeling
- Feature-selection stability
- Reproducibility assessment

### Libraries and Software

- scikit-learn
- scikit-survival
- pandas
- NumPy
- SciPy
- lifelines
- GEOparse
- matplotlib
- ggplot2
- SAS
- SPSS
- Minitab
- Power BI
- Tableau
- Microsoft Excel

---

## Education

### Georgia State University
**M.S. in Applied Statistics**  
Concentration: Machine Learning and Data Science  
Expected May 2028

### The University of Akron
**M.S. in Statistics**  
May 2026  

Research Advisor: Professor Sujay Datta

### University of Cape Coast
**B.Sc. in Mathematics and Statistics**  
August 2023

---

## Teaching and Academic Experience

### Graduate Teaching Assistant
**Department of Statistics, The University of Akron**  
August 2024 – May 2026

- Led weekly statistics laboratories
- Tutored students in statistics, probability, R, SPSS, and Minitab
- Graded assignments and assessments
- Supported quantitative problem solving and statistical software instruction

### Teaching Assistant
**University of Cape Coast**  
September 2023 – July 2024

- Tutored undergraduate students in statistics and quantitative methods
- Supported grading and instructional activities

---

## Professional Memberships

- American Statistical Association
- University of Akron Statistical Association

---

## Research Direction

My research is increasingly centered on a fundamental question in biomedical machine learning:

> **When can we trust a predictive model, its performance estimate, and the biological features or explanations it produces?**

I am particularly interested in developing statistical and machine-learning frameworks that evaluate not only predictive accuracy, but also:

- stability
- reproducibility
- calibration
- generalization
- uncertainty
- interpretability
- robustness to sample size and dimensionality
- reliability of multimodal integration

The long-term objective is to contribute reliable and clinically meaningful AI methods for cancer prediction and biomedical decision support.

---

## Connect

- [LinkedIn](https://www.linkedin.com/in/ackaah-enock-kumi)
- [GitHub](https://github.com/Enock-ackaah)
- Email: [kumiackaahenock@gmail.com](mailto:kumiackaahenock@gmail.com)
