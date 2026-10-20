# SurfaceGuard AI: Industrial Surface Anomaly Segmentation

## Student Details
- **Name:** 24f3004403
- **ID / Username:** 24f3004403@ds.study.iitm.ac.in

## GitHub Repo Setup
This repository is created for the DL and GenAI project and is intended to follow milestone-based development.

### Initial Folder Structure (empty placeholders)
```
DL-Genai-Project-Sept-26/
├── scripts/
├── notebooks/
└── data/
```

> Actual code, notebooks, and datasets will be added in later project milestones.

---

## Introduction to DL and GenAI Project [BSDA2001P] – Repository Guidelines
Welcome to the official project repository template.

This document defines the mandatory Git workflow and repository structure that must be followed throughout the course. These guidelines form part of the evaluation criteria.

### Purpose of This Structure
This repository structure ensures:
- Clear milestone-wise progress tracking
- Proper version control practices
- Transparent academic evaluation
- Reproducibility of work
- Professional software engineering discipline

## Branching Strategy (Mandatory)

### 1. Main Branch (`main`)
The `main` branch must always contain:
- Latest working notebook
- Final training script
- Final inference script
- Updated reports
- `README` file
- Any deployment or utility scripts

The `main` branch should always represent the most stable and updated version of your project.

### 2. Milestone Branches (Strict Requirement)
For every milestone, you must:
- Create a new branch
- Perform all milestone-related work inside that branch
- Commit milestone-specific code only in that branch
- Push the branch to the remote repository

### Branch Naming Convention
Use the following format:
- `milestone-1`
- `milestone-2`
- `milestone-3`

Example:
```bash
git checkout -b milestone-1
```

### Strict Rules
#### Do Not Delete Milestone Branches
Even after merging into `main`, milestone branches must remain in the repository for:
- Evaluation
- Progress tracking
- Audit purposes

Deleting milestone branches will lead to penalties.

#### Do Not Commit Milestone Work Directly to `main`
All milestone development must first happen inside the corresponding milestone branch.

## Recommended Workflow
### Step 1: Create a Milestone Branch
```bash
git checkout main
git pull origin main
git checkout -b milestone-1
```

### Step 2: Work on the Milestone
- Add notebooks
- Add scripts
- Add documentation
- Commit regularly

```bash
git add .
git commit -m "Milestone 1: Completed data preprocessing and EDA"
```

### Step 3: Push the Branch
```bash
git push origin milestone-1
```

### Step 4: Merge into Main (After Completion)
Once the milestone is complete:

```bash
git checkout main
git merge milestone-1
git push origin main
```

Do not delete the milestone branch after merging.

## Suggested Repository Structure
```text
project-name/
│
├── notebooks/
│   ├── milestone-1.ipynb
│   ├── milestone-2.ipynb
│   └── final_notebook.ipynb
│
├── src/
│   ├── train.py
│   ├── inference.py
│   └── utils.py
│
├── reports/
│   ├── milestone-1-report.pdf
│   ├── milestone-2-report.pdf
│   └── final-report.pdf
│
├── models/
│
├── requirements.txt
└── README.md
```

## Best Practices
- Commit frequently with meaningful messages
- Keep milestone code reproducible
- Avoid committing unnecessary large files
- Use `.gitignore` properly
- Maintain a clean and structured repository

## Commit Message Guidelines
### Good Example
`Milestone 2: Implemented feature engineering and baseline model`

### Poor Examples
- `update`
- `changes`
- `final`

## Evaluation Criteria
Your grading will consider:
- Proper branch usage
- Clear milestone separation
- Code organization
- Reproducibility
- Professional Git practices

Failure to follow the branching policy may result in grade deductions.

## Final Note
This workflow mirrors real-world industry development practices.

By following it properly, you demonstrate:
- Ownership
- Engineering maturity
- Clean project tracking
- Professional development standards

If you have any doubts, clarify before proceeding.

---

## Project Overview
Modern manufacturing relies on automated visual inspection to catch quality issues before products leave the production line.

In this competition, the goal is to build an AI inspection system that:
- Finds surface anomalies in industrial images
- Identifies anomaly type/category
- Marks exactly which pixels are anomalous (pixel-level segmentation)

The system must handle four anomaly categories and should avoid false positives while maximizing mask accuracy.
