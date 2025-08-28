# 🚀 DBL Project Template

This guide is meant for students joining the DBL.  

Follow the instructions and contact your supervisor or [laugon@dtu.dk](mailto:laugon@dtu.dk) if you have any questions :)

Welcome new student!

---

## 0. Before you start
As a member of the DBL, your project will have a **project ID** that looks like `DBL123` (e.g. *DBL046*).  
Ask your supervisor to find out what your project ID is.  

Once you have access to [DTU's HPC](https://www.hpc.dtu.dk/?page_id=497), login to the HPC. This is your **home folder**.  

1. Access HPC.  
2. Inside your home directory, create a **work directory** named after your `projectID_nameID` (e.g. `DBL046_johndoe`).  
   This is the folder where you’ll be working from now on.  

Example:
```bash
cd ~
mkdir DBL046_johndoe
cd DBL046_johndoe
```
---

## 1. Create your new project repository
1. Go to this template’s GitHub page.  
2. Click the green **“Use this template”** button → **“Create a new repository”**.  
3. Name your new repo with project identifier and DTU name in your credentials (e.g. `DBL123_johndoe`).  
4. Click **Create repository**.  

You now have your **own copy** of this structure on GitHub.  

---

## 2. Get the project onto your computer or HPC

Navigate to your project mother folder in the HPC or your local computer (e.g. DBL000).

### Option A — Using Git
```bash
git clone https://github.com/<your-github-username>/<your-new-DBL-project-repo>.git
cd <your-new-repo>
```
note: it should look like https://github.com/johnsgit9/DBL123_johndoe.git

### Option B — Download as ZIP
On your repo page, click Code → Download ZIP.
Unzip it and manually move the folder where you want it.


## 3. Set up the Python environment

This template includes a minimal Conda environment file (environment.yml).
You can use it to create a consistent Python environment:
```bash
conda env create -f environment.yml
conda activate labproj
```

## 4. Folder structure
```bash
project_name/
├── README.md             # Overview and clear instructions on how to run
├── LICENSE               # (if open source or shared)
├── environment.yml       # or requirements.txt / pyproject.toml
├── data/                 # Raw or processed data (usually .gitignored)
│   ├── raw/              # Untouched data
├── notebooks/            # Jupyter/Colab notebooks for exploration
├── src/                  # Reusable code (functions, classes, modules) "shelf"
│   ├── __init__.py
│   ├── config.py
│   ├── preprocessing.py
│   └── plotting.py      
│   └── utils/            # Reusable helper functions
├── scripts/              # sequential pipeline steps "recipe"
│   ├── 00_sumbit.sh
│   ├── 01_preprocess.py
│   ├── 02_train.py
│   └── 03_plot_results.py
├── tmp/                  # Unit tests / experiment validation
├── results/              # Outputs (figures, logs, metrics)
│   ├── figures/
│   └── logs/
└── docs/                 # Project documentation (.ppt, posters, manuscripts)
```

