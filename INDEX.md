# Submission Contents

| Path | What it is |
|---|---|
| `output/matching_results.tsv` | Final entity matches — scored on the leaderboard |
| `output/candidate_pairs.tsv` | Final candidate set fed to the matching model |
| `code/business_entity_resolution/src/pipeline.ipynb` | Full, runnable pipeline (Kaggle notebook) |
| `code/business_entity_resolution/README.md` | Reproduce instructions and pipeline overview |
| `code/business_entity_resolution/requirements.txt` | Pinned dependencies |
| `Documentation_template.docx` | Full methodology write-up (blocking, features, model, results) |

**Model:** scikit-learn `HistGradientBoostingClassifier` · **Decision threshold:** see `entity_matcher_threshold.txt` value in the methodology doc
**Infrastructure:** Kaggle notebook + local SQLite blocking index (no external APIs or lookups)
