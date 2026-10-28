# MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project

[![Python](https://img.shields.io/badge/Python-3.12%2B-3776AB?logo=python&logoColor=white)](https://github.com/python/cpython)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://github.com/jupyter/notebook)
[![NumPy](https://img.shields.io/badge/NumPy-2.1.3-013243?logo=numpy&logoColor=white)](https://github.com/numpy/numpy)
[![Pandas](https://img.shields.io/badge/Pandas-2.2.3-150458?logo=pandas&logoColor=white)](https://github.com/pandas-dev/pandas)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.9.2-11557C)](https://github.com/matplotlib/matplotlib)
[![SciPy](https://img.shields.io/badge/SciPy-1.14.1-8CAAE6?logo=scipy&logoColor=white)](https://github.com/scipy/scipy)
[![Statsmodels](https://img.shields.io/badge/Statsmodels-0.14.4-4051B5)](https://github.com/statsmodels/statsmodels)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI-2088FF?logo=githubactions&logoColor=white)](https://github.com/features/actions)
[![VS Code](https://img.shields.io/badge/VS%20Code-Notebook%20Workflow-007ACC?logo=visualstudiocode&logoColor=white)](https://github.com/microsoft/vscode)

> **Academic EDA project:** four structured datasets analyzed with rigorous exploratory data analysis, statistical summaries, visualization, outlier detection, relationship analysis, and evidence-based brainstorming.

## Table of Contents

- [Project Overview](#project-overview)
- [Four Notebooks](#four-notebooks)
- [Repository Structure](#repository-structure)
- [Technology Stack](#technology-stack)
- [Prerequisites](#prerequisites)
- [macOS Setup](#macos-setup)
- [Windows Setup](#windows-setup)
- [VS Code Setup](#vs-code-setup)
- [Execute All Four Notebooks](#execute-all-four-notebooks)
- [Execute Individual Notebooks](#execute-individual-notebooks)
- [GitHub Actions Workflow](#github-actions-workflow)
- [Expected Outputs](#expected-outputs)
- [Troubleshooting](#troubleshooting)
- [GitHub Workflow and Repository Links](#github-workflow-and-repository-links)
- [Academic / Reproducibility Notes](#academic--reproducibility-notes)

---

## Project Overview

This repository contains four Jupyter Notebook projects prepared around the supplied datasets and their corresponding analytical tasks:

1. **Manufacturing Energy Consumption — Regression**
2. **Port Logistics Dispatching — Classification**
3. **E-Commerce Sales & Customer Insights — EDA / Shipping Fee Analysis**

The notebooks follow a common EDA structure:

- understand the big picture of the dataset;
- inspect dimensions, data types and missing values;
- understand categorical variables;
- understand numerical variables and distributions;
- detect and investigate outliers;
- analyze relationships among variables;
- formulate findings, hypotheses and research questions;
- support methodological decisions with appropriate references.

### Canonical Manufacturing notebook

Two Manufacturing notebook versions were created during development. The repository uses the **`_with_saved_plots`** version as the canonical executable notebook so that the four-notebook workflow contains exactly one Manufacturing notebook.

---

## Four Notebooks

| # | Notebook | Analytical task | Dataset file |
|---|---|---|---|
| 1 | `DASCM_2026_Part1_Manufacturing_Energy_Consumption_EDA_FINAL_REVISED.ipynb` | Manufacturing Energy Consumption — Regression | `regression_manufacturing.csv` |
| 2 | `DASCM_2026_Part1_Port_Logistics_Dispatching_EDA_FINAL_REVISED.ipynb` | Port Logistics Dispatching — Classification | `classification_logistics.csv` |
| 3 | `DASCM_2026_Part1_ECommerce_Sales_Customer_Insights_EDA.ipynb` | E-Commerce Sales & Customer Insights — Shipping Fee | `realistic_e_commerce_sales_data.csv` |

### Dataset 1 — Manufacturing Energy Consumption

Regression-oriented EDA for predicting `Energy_Consumption_kWh`. The analytical framing considers production, machine condition, maintenance, human and environmental factors and explicitly investigates nonlinear patterns described in the project specification.

### Dataset 2 — Port Logistics Dispatching

Classification-oriented EDA for the six-class `Recommended_Dispatch_Action` target:

- `PROCEED_AS_PLANNED`
- `WAIT_AND_MONITOR`
- `RESCHEDULE_SLOT`
- `REROUTE`
- `REASSIGN_VEHICLE`
- `PRIORITY_RECOVERY`

### Dataset 3 — E-Commerce Sales & Customer Insights

EDA for predicting `Shipping Fee` using product, customer, geographic and order characteristics. The notebook explicitly audits `Total Price` against `Unit Price × Quantity` before making the leakage/redundancy decision.

---

## Repository Structure

```text
MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project/
│
├── README.md
├── requirements.txt
├── regression_manufacturing.csv
├── classification_logistics.csv
├── realistic_e_commerce_sales_data.csv
│
├── DASCM_2026_Part1_Manufacturing_Energy_Consumption_EDA_FINAL_REVISED.ipynb
├── DASCM_2026_Part1_Port_Logistics_Dispatching_EDA_FINAL_REVISED.ipynb
├── DASCM_2026_Part1_ECommerce_Sales_Customer_Insights_EDA.ipynb
│
├── .github/
│   └── workflows/
│       └── notebooks.yml
│
└── executed_notebooks/
    └── # generated when notebooks are executed
```

The datasets are kept at repository root intentionally because the notebooks use relative paths such as `Path.cwd()` or `Path("regression_manufacturing.csv")`.

---

## Technology Stack

The project uses the following open-source technologies. The links below point to the **official GitHub repositories**, not third-party mirrors.

| Technology | Purpose | Official GitHub repository |
|---|---|---|
| **Python** | Programming language | [python/cpython](https://github.com/python/cpython) |
| **Jupyter Notebook** | Interactive notebook environment | [jupyter/notebook](https://github.com/jupyter/notebook) |
| **NumPy** | Numerical computing | [numpy/numpy](https://github.com/numpy/numpy) |
| **Pandas** | Data manipulation and analysis | [pandas-dev/pandas](https://github.com/pandas-dev/pandas) |
| **Matplotlib** | Statistical/data visualization | [matplotlib/matplotlib](https://github.com/matplotlib/matplotlib) |
| **Seaborn** | Statistical visualization | [mwaskom/seaborn](https://github.com/mwaskom/seaborn) |
| **SciPy** | Statistical analysis | [scipy/scipy](https://github.com/scipy/scipy) |
| **Statsmodels** | Statistical modelling and tests | [statsmodels/statsmodels](https://github.com/statsmodels/statsmodels) |
| **VS Code** | Development environment | [microsoft/vscode](https://github.com/microsoft/vscode) |
| **Git** | Version control | [git/git](https://github.com/git/git) |
| **GitHub Actions** | Continuous integration / notebook execution | [actions](https://github.com/actions) |

### Core dependency versions

```text
Python       3.12.x recommended
NumPy        2.1.3
Pandas       2.2.3
Matplotlib   3.9.2
Seaborn      0.13.2
SciPy        1.14.1
Statsmodels  0.14.4
Jupyter      1.1.1
Notebook     7.2.2
nbconvert    7.16.4
ipykernel    6.29.5
```

> `requirements.txt` is the reproducibility source of truth for the consolidated repository environment.

---

## Prerequisites

Install the following before starting:

- **Python 3.12.x**
- **Git**
- **Visual Studio Code** (recommended)
- **VS Code Python extension**
- **VS Code Jupyter extension**

### Official installation resources

- Python: <https://www.python.org/downloads/>
- Git: <https://git-scm.com/downloads>
- VS Code: <https://code.visualstudio.com/download>
- Python extension: <https://marketplace.visualstudio.com/items?itemName=ms-python.python>
- Jupyter extension: <https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter>

---

# macOS Setup

## Step 1 — Install/check Python

Open **Terminal**:

```bash
python3 --version
```

Recommended result:

```text
Python 3.12.x
```

If Python is not installed, install it from the official Python distribution or Homebrew:

```bash
brew install python@3.12
```

Then verify:

```bash
python3.12 --version
```

## Step 2 — Clone the GitHub repository

Replace `<YOUR-REPOSITORY-URL>` with your actual GitHub repository URL:

```bash
git clone https://github.com/Subiswas36218/MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project
cd MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project
```

If the repository is already downloaded:

```bash
cd /path/to/MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project
```

## Step 3 — Create a virtual environment

```bash
python3.12 -m venv venv
```

Activate it:

```bash
source venv/bin/activate
```

You should see something similar to:

```text
(.venv) user@Mac ... $
```

## Step 4 — Upgrade pip

```bash
python -m pip install --upgrade pip
```

## Step 5 — Install all dependencies

```bash
python -m pip install -r requirements.txt
```

## Step 6 — Register the Jupyter kernel

```bash
python -m ipykernel install --user --name dascm-2026 --display-name "Python (DASCM 2026)"
```

## Step 7 — Verify the environment

```bash
python -c "import numpy, pandas, matplotlib, seaborn, scipy, statsmodels; print('DASCM environment OK')"
```

## Step 8 — Launch Jupyter

```bash
jupyter notebook
```

or:

```bash
jupyter lab
```

---

# Windows Setup

## Step 1 — Install/check Python

Open **PowerShell**:

```powershell
py --version
```

or:

```powershell
python --version
```

Recommended result:

```text
Python 3.12.x
```

Install Python from:

<https://www.python.org/downloads/windows/>

During installation, enable **Add Python to PATH** when using the standard installer.

## Step 2 — Clone the GitHub repository

```powershell
git clone https://github.com/Subiswas36218/MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project
cd MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project
```

If the repository is already downloaded:

```powershell
cd C:\path\to\MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project
```

## Step 3 — Create a virtual environment

```powershell
py -3.12 -m venv venv
```

## Step 4 — Activate the environment

PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

If PowerShell blocks the activation script, use:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Then activate again:

```powershell
.\venv\Scripts\Activate.ps1
```

### Command Prompt alternative

If using `cmd.exe` instead of PowerShell:

```cmd
venv\Scripts\activate.bat
```

## Step 5 — Upgrade pip

```powershell
python -m pip install --upgrade pip
```

## Step 6 — Install dependencies

```powershell
python -m pip install -r requirements.txt
```

## Step 7 — Register the Jupyter kernel

```powershell
python -m ipykernel install --user --name dascm-2026 --display-name "Python (DASCM 2026)"
```

## Step 8 — Verify the environment

```powershell
python -c "import numpy, pandas, matplotlib, seaborn, scipy, statsmodels; print('DASCM environment OK')"
```

## Step 9 — Launch Jupyter

```powershell
jupyter notebook
```

or:

```powershell
jupyter lab
```

---

# VS Code Setup

## Step 1 — Open the repository

In VS Code:

**File → Open Folder → `MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project`**

Or from Terminal/PowerShell:

```bash
code .
```

## Step 2 — Install VS Code extensions

Install:

1. **Python** — Microsoft
2. **Jupyter** — Microsoft

## Step 3 — Select the virtual environment

Open the Command Palette:

```text
Cmd + Shift + P    # macOS
Ctrl + Shift + P   # Windows
```

Select:

```text
Python: Select Interpreter
```

Choose:

```text
venv/bin/python          # macOS
venv\Scripts\python.exe # Windows
```

## Step 4 — Select the Jupyter kernel

Open any `.ipynb` file and select:

```text
Python (DASCM 2026)
```

from the kernel selector in the notebook interface.

## Step 5 — Run the notebook

Use either:

- **Run All** from the notebook toolbar; or
- execute cells sequentially using `Shift + Enter`.

Always execute the notebook from the repository root so the relative dataset paths resolve correctly.

---

# Execute All Four Notebooks

## Recommended local method — macOS/Linux

After activating `venv` and from the repository root:

```bash
mkdir -p executed_notebooks
```

Then execute all four explicitly:

```bash
jupyter nbconvert --to notebook --execute --ExecutePreprocessor.timeout=1200 --output-dir executed_notebooks DASCM_2026_Part1_Manufacturing_Energy_Consumption_EDA_FINAL_REVISED.ipynb
```

```bash
jupyter nbconvert --to notebook --execute --ExecutePreprocessor.timeout=1200 --output-dir executed_notebooks DASCM_2026_Part1_Port_Logistics_Dispatching_EDA_FINAL_REVISED.ipynb
```

```bash
jupyter nbconvert --to notebook --execute --ExecutePreprocessor.timeout=1200 --output-dir executed_notebooks DASCM_2026_Part1_ECommerce_Sales_Customer_Insights_EDA.ipynb
```

The original notebooks remain unchanged; executed copies are written to `executed_notebooks/`.

## Windows PowerShell

Create the output directory:

```powershell
New-Item -ItemType Directory -Force executed_notebooks
```

Execute each notebook:

```powershell
jupyter nbconvert --to notebook --execute --ExecutePreprocessor.timeout=1200 --output-dir executed_notebooks DASCM_2026_Part1_Manufacturing_Energy_Consumption_EDA_FINAL_REVISED.ipynb
```

```powershell
jupyter nbconvert --to notebook --execute --ExecutePreprocessor.timeout=1200 --output-dir executed_notebooks DASCM_2026_Part1_Port_Logistics_Dispatching_EDA_FINAL_REVISED.ipynb
```

```powershell
jupyter nbconvert --to notebook --execute --ExecutePreprocessor.timeout=1200 --output-dir executed_notebooks DASCM_2026_Part1_ECommerce_Sales_Customer_Insights_EDA.ipynb
```

## Verify execution

A successful command ends without a Python traceback and produces an executed notebook under:

```text
executed_notebooks/
```

---

# Execute Individual Notebooks

## 1. Manufacturing Energy Consumption

```bash
jupyter notebook DASCM_2026_Part1_Manufacturing_Energy_Consumption_EDA_FINAL_REVISED.ipynb
```

Dataset:

```text
regression_manufacturing.csv
```

Target:

```text
Energy_Consumption_kWh
```

## 2. Port Logistics Dispatching

```bash
jupyter notebook DASCM_2026_Part1_Port_Logistics_Dispatching_EDA_FINAL_REVISED.ipynb
```

Dataset:

```text
classification_logistics.csv
```

Target:

```text
Recommended_Dispatch_Action
```

## 3. E-Commerce Sales & Customer Insights

```bash
jupyter notebook DASCM_2026_Part1_ECommerce_Sales_Customer_Insights_EDA.ipynb
```

Dataset:

```text
realistic_e_commerce_sales_data.csv
```

Target:

```text
Shipping Fee
```

The notebook explicitly audits `Total Price` before using it in the EDA/modeling discussion.

---

# GitHub Actions Workflow

The repository includes:

```text
.github/workflows/notebooks.yml
```

The workflow is configured to run when:

- code is pushed to `main`;
- a pull request targets `main`;
- the workflow is manually started with **Run workflow**.

The workflow:

1. checks out the repository;
2. provisions Python 3.12 on an Ubuntu GitHub-hosted runner;
3. installs the pinned dependencies from `requirements.txt`;
4. executes all four notebooks;
5. writes executed copies to `executed_notebooks/`;
6. uploads the executed notebooks as a GitHub Actions artifact.

This follows the GitHub Actions model in which workflows are YAML files stored under `.github/workflows/`. GitHub documents workflow status badges as a standard way to expose workflow health in a repository README.

### Workflow file

```text
.github/workflows/notebooks.yml
```

### Manually run the workflow

On GitHub:

```text
Repository
→ Actions
→ Execute DASCM 2026 Notebooks
→ Run workflow
```

### Add the repository-specific workflow status badge

Once this repository has been pushed to GitHub, GitHub can generate the exact status-badge Markdown for the workflow. The repository-specific form is:

```markdown
[![Execute DASCM 2026 Notebooks](https://github.com/Subiswas36218/MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project/actions/workflows/notebooks.yml/badge.svg)](https://github.com/Subiswas36218/MSCM-CO-07_Data-Analytics-in-Supply-Chain-Management_Team_Project/actions/workflows/notebooks.yml)
```

Replace `OWNER/REPOSITORY` with the actual GitHub repository path. Do **not** leave the placeholder in the final public README.

GitHub's official documentation explains that workflow badges can be added to a README and that the badge reflects the workflow status for the repository's default branch.

---

# Expected Outputs

The notebooks generate EDA artifacts such as:

- descriptive-statistics tables;
- missing-value summaries;
- categorical distributions;
- histograms;
- KDE/distribution plots;
- box plots;
- violin plots;
- outlier summaries;
- correlation heatmaps;
- pair/scatter analyses;
- parallel-coordinate views;
- bubble charts;
- category/region comparisons;
- temporal analyses;
- statistical relationship checks;
- brainstorming findings and hypotheses.

Where the notebook contains a `plots/` directory or saves figures, those outputs are produced relative to the notebook/project working directory.

---

# Troubleshooting

## `ModuleNotFoundError`

Make sure the virtual environment is active and reinstall dependencies:

```bash
python -m pip install -r requirements.txt
```

Verify the active interpreter:

```bash
python --version
python -c "import sys; print(sys.executable)"
```

## Jupyter is not recognized

Run it through Python:

```bash
python -m jupyter notebook
```

or reinstall:

```bash
python -m pip install jupyter notebook nbconvert ipykernel
```

## Wrong kernel in VS Code

Use:

```text
Command Palette
→ Python: Select Interpreter
→ .venv
```

Then open the notebook and select:

```text
Python (DASCM 2026)
```

## Dataset not found

Run the notebook from the repository root. Confirm that the expected CSV is beside the notebook:

```text
regression_manufacturing.csv
classification_logistics.csv
realistic_e_commerce_sales_data.csv
```

## Windows PowerShell activation error

Run:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Then:

```powershell
.\venv\Scripts\Activate.ps1
```

## GitHub Actions fails but local execution works

Check:

1. the dataset CSVs were committed to the repository;
2. the filenames match exactly, including capitalization;
3. `requirements.txt` is committed;
4. `.github/workflows/notebooks.yml` is committed;
5. the Actions run log identifies the failing notebook/cell.

---

# GitHub Workflow and Repository Links

### Official GitHub documentation

- [GitHub Actions](https://docs.github.com/en/actions)
- [GitHub Actions workflows](https://docs.github.com/en/actions/concepts/workflows-and-actions/workflows)
- [GitHub workflow syntax](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax)
- [GitHub workflow status badges](https://docs.github.com/en/actions/how-tos/monitor-workflows/add-a-status-badge)
- [GitHub-hosted runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners)

### Official technology repositories

- [Python](https://github.com/python/cpython)
- [Jupyter Notebook](https://github.com/jupyter/notebook)
- [NumPy](https://github.com/numpy/numpy)
- [Pandas](https://github.com/pandas-dev/pandas)
- [Matplotlib](https://github.com/matplotlib/matplotlib)
- [Seaborn](https://github.com/mwaskom/seaborn)
- [SciPy](https://github.com/scipy/scipy)
- [Statsmodels](https://github.com/statsmodels/statsmodels)
- [VS Code](https://github.com/microsoft/vscode)
- [Git](https://github.com/git/git)
- [GitHub Actions](https://github.com/actions)

---

# Academic / Reproducibility Notes

- The original supplied datasets are preserved without modification.
- The notebooks are intended to be executed from the repository root.
- The project uses a pinned Python dependency environment for reproducibility.
- EDA does not automatically imply causality.
- Outliers are investigated rather than automatically deleted.
- Missing values are explicitly reported before any later modeling treatment.
- Potential target leakage is assessed explicitly where the project specification identifies leakage-risk variables.
- The GitHub Actions workflow provides a repeatable CI execution path for all four notebooks.

## Recommended Git workflow

```bash
git status
git add .
git commit -m "Add DASCM 2026 four-dataset EDA notebooks"
git push origin main
```

After pushing, open the **Actions** tab on GitHub to verify that the four-notebook workflow completes successfully.

---

## License / Academic Use

Unless a separate license is added to the repository, treat this repository as an academic project and preserve the original dataset/source attribution requirements applicable to the supplied materials.
