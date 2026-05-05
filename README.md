# ai-programming-foundations-project

# AI Career Compass - DACH Job Market Analysis
This project explores the AI job market across Germany, Austria and Switzerland using live data collected from the Adzuna Jobs API. It covers a broad spectrum of AI roles — from engineering and data science to consulting, product management and system integration - and identifies patterns in role demand, hiring locations and salary transparency across the DACH region.
Dataset: Adzuna DACH AI Job Postings (scraped May 2025, 442 rows)
Collected via the Adzuna Jobs API using fetch_ai_jobs.py.

## How to Run the Project
1. Clone the repository
bashgit clone https://github.com/n1n4ch/ai-programming-foundations-project.git
cd ai-programming-foundations-project
2. Install dependencies
bashpip install -r requirements.txt
3. Fetch the dataset (optional — CSV already included)
bashpython fetch_ai_jobs.py
4. Open and run the notebook
bashjupyter notebook data_workflow.ipynb
Run all cells in order using Kernel → Restart & Run All.

## Requirements
Generate with:
pip freeze > requirements.txt
