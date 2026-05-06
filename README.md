# ai-programming-foundations-project

# AI Career Compass — DACH Job Market Analysis

This project explores the AI job market across Germany, Austria, and Switzerland using live data collected from the Adzuna Jobs API. It covers a broad spectrum of AI roles — from engineering and data science to consulting, product management, and system integration — and identifies patterns in role demand, hiring locations, and salary transparency across the DACH region. The dataset and workflow are designed to scale across future modules: the job description text supports NLP and deep learning, the role categories support classification models and the API collection script can be extended into an autonomous data pipeline.

**Dataset:** Adzuna DACH AI Job Postings, scraped May 2025 (442 rows)  
**Source:** Collected via the [Adzuna Jobs API](https://developer.adzuna.com) using `fetch_ai_jobs.py`

---

## How to Run the Project

**1. Clone the repository**

```
git clone https://github.com/n1n4ch/ai-programming-foundations-project.git
cd ai-programming-foundations-project
```

**2. Install dependencies**

```
pip install -r requirements.txt
```

**3. Fetch the dataset** *(optional — CSV already included)*

```
python fetch_ai_jobs.py
```

**4. Open and run the notebook**

```
jupyter notebook data_workflow.ipynb
```

Run all cells in order via **Kernel → Restart & Run All**

---

## Data Bias and Responsible Use

Poor data cleaning or collection decisions in this project could introduce misleading results in several ways. The dataset was collected via keyword-based API queries, meaning roles with non-standard titles are systematically excluded - AI Consulting roles in particular are underrepresented because many appear under German-language titles not covered by the search terms. Salary data is 96% missing and the employers who do disclose compensation are likely not representative of the full market, skewing any salary analysis toward international companies and startups. The single Swiss salary disclosure of 416,000 is in CHF rather than EUR, which artificially inflates cross-country salary comparisons if not handled explicitly. Finally, the dataset represents a single point in time and should not be used to draw conclusions about long-term hiring trends.

---

## Future Directions

The `description` column contains job posting text suitable for NLP preprocessing, sentence embeddings and role clustering in later deep learning modules. The `role_category` labels provide a ready-made target variable for supervised classification models. The `fetch_ai_jobs.py` script can be extended into an agentic data collection pipeline that refreshes the dataset autonomously, compares snapshots over time and surfaces emerging role trends - directly supporting the autonomous workflow design covered in Module 7.



## Requirements

Generate with:

```
pip freeze > requirements.txt
```
