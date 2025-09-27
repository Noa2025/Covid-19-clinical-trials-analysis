# Covid-19-clinical-trials-analysis
This repository contains an exploratory analysis of **COVID-19 clinical trials** using data from AACT (ClinicalTrials.gov).   
The project investigates **enrollment patterns**, **vaccine development**, **alternative treatments**, and **trial success rates** based on reported primary-endpoint results.
## Key Findings
| Topic | Highlights |
|------|------------|
| **Trial Landscape** | • Total trials: **9,764**<br>• Nearly half (**4,029**) reported no phase.<br>• **714** trials were Phase 3, with 226 completed. |
| **Enrollment** | • Total subjects enrolled: **374,487,794**.<br>• Largest trial (AstraZeneca Vaxzeria): **155,975,015** participants.<br>• Smallest trial enrolled just **1** subject. |
| **Vaccines** | • Vaccine trials accounted for **8%** of all trials but **48%** of total enrollment.<br>• Vaccine trial initiations peaked in **2021**.<br>• Largest sponsors: **Sinocelltech (13 trials)**, **BioNTech (12)**, **Moderna (10)**.<br>• Notable early terminations included **Inovio**, **CureVac**, and **AstraZeneca** trials. |
| **Study Results** | • Among **312 trials** with published results: **40% success**, **44% failure**, **16% unknown**.<br>• Industry-funded results: **59 success**, **76 fail**, **36 unknown**. |
| **Specific Interventions** | • Ivermectin: **3 success**, **2 fail**, **1 unknown**.<br>• Hydroxychloroquine: **1 success**, **4 fail**, **1 unknown**.<br>• Vaccines (with results): **4 success**, **3 fail**, **9 unknown**. |
| **Alternative Treatments** | Trials included **yoga (26)**, **meditation (15)**, **mindfulness (57)**, and **tai chi (2)**. |
## Data
* **Primary source**: AACT COVID-19 Spreadsheets, outcome and outcome_analyses tables.
* **Database**: SQLite database (`covid_trials.db`) with tables for trials, results (CTG-PVAL), and joined tables (`covid_with_results`).  
## Methods
1. **Data Loading** – Trials and results were imported into SQLite.  
2. **SQL Exploration** – Used Python + pandas to run queries such as:  
   * Trial counts by phase and masking method  
   * Enrollment distribution  
   * Vaccine trial proportions and yearly trends  
   * Industry sponsor analysis  
   * Study success/failure rates using p-values from the CTG-PVAL table  
3. **Filtering & Pattern Matching** – Case-insensitive (`LOWER`) matching to identify interventions (e.g., `%yoga%`, `%mindfulness%`).

## Tools
* Python: pandas, sqlite3, Jupyter Notebook
* Database: SQLite
