# Amazon ML Challenge 2026 — Business Entity Resolution

A large-scale entity resolution pipeline developed for the **Amazon ML Challenge 2026**.

The task involved identifying matching business entities across noisy, independent data sources. The project focused on scalable data cleaning, candidate generation, blocking, similarity features, and pairwise classification.

## What I worked on

- Cleaned and normalized large business datasets containing names, addresses, and country information.
- Built candidate-generation strategies using exact matching, token blocking, prefix indexing, and fuzzy matching.
- Developed memory-conscious workflows for processing millions of records under constrained compute resources.
- Trained a pairwise matching model using scikit-learn's `HistGradientBoostingClassifier`.
- Generated final entity-match and candidate-pair outputs for submission.

## Pipeline

1. **Data cleaning** — normalize Unicode, casing, punctuation, and text fields.
2. **Candidate generation / blocking** — reduce the number of possible record pairs using name/address indexes and blocking strategies.
3. **Feature generation** — calculate similarity features for candidate pairs.
4. **Model training** — train a gradient-boosted classifier to distinguish matching and non-matching pairs.
5. **Inference** — score candidate pairs and generate the final matching output.

## Repository contents

```text
.
├── README.md
├── requirements.txt
├── code/
│   └── pipeline.ipynb
└── docs/
    └── project-notes.md
```

## Reproducibility

The notebook was developed and run in a Kaggle notebook environment using Python 3.12. The original challenge dataset is **not included** in this repository because of its size and challenge restrictions.

Install the dependencies with:

```bash
pip install -r requirements.txt
```

The original challenge submission also produced large `matching_results.tsv` and `candidate_pairs.tsv` files. These are intentionally not stored in this GitHub repository because they are too large for normal GitHub hosting.

## Fair-play constraints

The solution did not use external data lookups, APIs, geocoding services, or third-party entity-resolution tools. The pipeline operated on the challenge-provided data.

## Technologies

Python · Pandas · NumPy · Scikit-learn · RapidFuzz · SQLite · Jupyter/Kaggle
