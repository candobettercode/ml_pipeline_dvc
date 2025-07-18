# 📧 Spam Detection using Machine Learning

## 🚀 Project Overview
This project implements a Spam Detection System using a machine learning pipeline built with RandomForestClassifier. The workflow follows best practices in MLOps for reproducibility and automation.

It leverages DVC for data and model versioning, pipeline management, and experiment tracking, alongside AWS S3 for remote storage.

# 🔍 Problem Statement
Classify emails/messages as Spam or Not Spam using machine learning techniques with high accuracy and maintain reproducibility across experiments.
## 🛠️ Tech Stack
- Python

- Scikit-learn (RandomForestClassifier)

- DVC (Data & Pipeline Versioning, Experiment Tracking)

- dvclive (Metrics Logging)

- AWS S3 (Remote Storage)

- GitHub (Version Control)

- VSCode (DVC Extension)

# 📂 Project Structure

```plaintext

├── data/ # Raw and processed data (gitignored)
├── models/ # Trained models (gitignored) 
├── reports/ # Evaluation reports, plots (gitignored) 
├── src/ # Source code modules 
│   ├── data/ # Data loading, splitting, preprocessing 
│   ├── features/ # Feature engineering 
│   ├── models/ # Training, evaluation scripts 
│   └── visualization/ # Visualization scripts (if any) 
├── dvc.yaml # DVC pipeline definition 
├── params.yaml # Model and pipeline parameters 
├── requirements.txt # Python dependencies 
├── README.md # Project documentation 
└── .gitignore `
```


# 🔄 Workflow
## Initial Setup
- Create and clone GitHub repo.
- Add src/ folder with modular components.
- Add data/, models/, reports/ to .gitignore.
- git add, commit, push.

## DVC Pipeline (Without Params)
- dvc init
- Create dvc.yaml defining stages.
- Run dvc repro
- Validate with dvc dag
- git add, commit, push

## DVC Pipeline (With Params)
- Create params.yaml
- Link params.yaml to dvc.yaml
- Run dvc repro
- git add, commit, push

## DVC Experiments with dvclive
- pip install dvclive
- Integrate dvclive for metrics logging
- Run experiments: dvc exp run
- Review results: dvc exp show
- Manage experiments: dvc exp apply, dvc exp remove
- git add, commit, push

## AWS S3 Remote Storage
- Setup AWS IAM user and S3 bucket
- Configure AWS CLI: aws configure
- pip install dvc[s3]
- dvc remote add -d dvcstore s3://your-bucket
- dvc push
- git add, commit, push

# 💡 Key Learnings
- End-to-end ML pipeline automation with DVC and GitHub

- Experiment tracking and model versioning with dvclive

- Managing reproducible ML workflows with params.yaml

- Integration of MLOps principles with AWS S3 for scalability

