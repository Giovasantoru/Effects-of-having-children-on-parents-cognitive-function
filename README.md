# Effects-of-having-children-on-parents-cognitive-function

Project Overview

This project replicates the dataset used in the research by Bonsang et al., which examines the impact of childbearing on cognitive decline in older adults. The data is derived from multiple waves of the Survey of Health, Ageing and Retirement in Europe (SHARE), specifically waves 1, 2, 4, 5, 6, and 8. The final dataset includes 92,748 observations. Using a two-stage least squares (2SLS) model and Pearl’s non-parametric bounds, we estimate the causal effect of having many children on cognitive performance. Additionally, a Principal Component Analysis (PCA) is employed to create a cognitive score index.

Project Structure
The analysis is conducted across several R script files:

Modelli dataset final.Rdm – Contains the statistical models and analyses.
database wave 8.Rdm – Prepares and processes the dataset for the analysis.
Descriptive Statistic.Rdm – Visualizes and describes the dataset with various graphs and tables.

Dataset Waves
Wave 1: Baseline (2004-2005)
Wave 2: Follow-up (2006-2007)
Wave 4: (2011)
Wave 5: (2013)
Wave 6: (2015)
Wave 8: Added for extra statistical power (2020)

Key Libraries
The following R libraries are utilized in the project: 
library(tidyverse)
library(AER)
library(lmtest)
library(sandwich)
library(ggplot2)
library(haven)
library(tidyr)
library(stats)
library(bpbounds)

Code Workflow
Below is an outline of the workflow for processing and analyzing the dataset:

Reading and Preparing Data:
SHARE datasets for each wave are read using haven::read_dta().
Cognitive and childbearing variables are cleaned and aligned across waves.
Combining Waves:
Data from each wave (1, 2, 4, 5, 6, 8) is merged on mergeid, ensuring consistency across waves.
Handling Missing Data:
Missing data is handled using mutate() and coalesce() to fill missing cognitive or childbearing variables where necessary.
Principal Component Analysis (PCA):
Conducted on cognitive measures to create a cognitive index using prcomp().
2SLS Estimation:
The impact of multiple children on cognitive decline is estimated using 2SLS models.
Non-Parametric Bounds:
Pearl’s non-parametric bounds technique is applied to refine the causal estimates.

# Key Findings and Results
Cognitive Scores and Family Size: The analysis found that the number of children in a family and their sex composition have a statistically significant effect on cognitive outcomes, particularly for verbal fluency and immediate recall.
Education Impact: Education level also plays a critical role in determining cognitive performance.
Instrumental Variables Estimation: The IV model confirms the importance of exogenous variation (e.g., sex composition of children) in identifying the causal effect of having more children on cognitive outcomes.

Next Steps
Further Model Validation: Validate the IV results with alternative instruments and robustness checks.
Policy Implications: Explore the broader social and policy implications of the results, particularly in relation to family planning and cognitive health interventions.
