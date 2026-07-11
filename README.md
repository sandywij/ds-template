# 🚀 Quickstart Guide: Data Journalism Project \[Project Name]

Welcome! This repository provides a structured environment built for rapid data exploration and reproducible analysis. Follow these three phases in order to get started.

---

## 🟢 Phase 1: Setup & Environment
You must create an isolated sandbox environment first.

### 1. Clone Repository
```bash
git clone [repo-url]
cd data_journalism_project
```

### 2. Create Venv (Virtual Environment)
This isolates the project dependencies from your global Python installation.
```bash
python3 -m venv .venv
# Activate:
# Mac/Linux: source .venv/bin/activate
# Windows: .\venv\Scripts\activate
```

### 3. Install Dependencies
Install all required libraries defined in the manifest file.
```bash
pip install -r requirements.txt
```

---

## 🛠️ Phase 2: The Workflow (Analysis Pipeline)
Follow these steps sequentially. **The output of one step feeds directly into the next.**

### Step A: Clean Data (Preprocessing)
Run this script first to clean and standardize your raw input data. This creates the stable "Golden Copy."
```bash
python 02_scripts/data_preprocessing.py
# ✅ OUTPUT: 'results/cleaned_data.csv' 
```

### Step B: Explore & Visualize (Analysis)
Open JupyterLab and run your hypothesis testing in the notebook, always referencing the clean file created above.
*   `jupyter lab`
*   Open `03_notebooks/exploration.ipynb`

**(Action: Run code to generate all figures and charts. Save these assets into the `results/` directory.)**

### Step C: Deliver (The Story)
Collect your validated findings from the `results/` folder—your final charts, tables, and derived metrics—and use them to write your narrative article.

***

## 📂 Quick Reference Map

| Folder | Content | Role | Key Rule |
| :--- | :--- | :--- | :--- |
| **`01_data/`** | Raw source files. | **Input.** | ⚠️ **DO NOT TOUCH THIS FOLDER.** |
| **`02_scripts/`** | Clean-up code. | **Process.** (Runs the core transformation logic). | Run this first! |
| **`03_notebooks/`** | Scratchpad notebooks. | **Discover.** (Where you test ideas iteratively.) | Use for discovery, save outputs elsewhere. |
| **`results/`** | Final figures and data. | **Output.** (The final assets used in your article). | Everything must live here. |
