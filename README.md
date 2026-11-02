# Hanta — Embedding-based Drug–Virus Repurposing

Research project to rank candidate small-molecule drugs against viruses using **drug and virus embeddings** with a neural-network predictor.

## Planned pipeline

1. Curate drug SMILES, viral sequences, metadata and experimental associations.
2. Extract drug representations with MoLFormer.
3. Extract a single representation per virus with a viral sequence encoder (HViLM candidate) and hierarchical mean pooling across sequence windows and segments.
4. Combine drug and virus embeddings in a neural-network pair classifier.
5. Evaluate with leakage-aware splits and compare against the earlier similarity-based baseline.
6. Rank candidate drug–virus pairs for subsequent biological validation.

**Status:** initial repository scaffold; data quality controls, models and experiments are not yet completed.

## Repository organization

- `configs/`: experiment settings
- `data/raw/`: original source files (local by default)
- `data/interim/`: intermediate sequence and metadata processing
- `data/processed/`: curated pairs, train/validation/test splits and embeddings
- `data/legacy/`: previous similarity-based outputs for benchmarking
- `src/`: data preparation, embedding, neural-network, training, evaluation and prediction code
- `notebooks/`: exploratory experiments
- `scripts/`: local setup helpers
- `docs/`: methodology and file inventory
- `tests/`: automated tests
- `checkpoints/`, `outputs/`: generated runs, model weights and predictions

## Data policy

**This is a public repository.** Do not commit private, restricted, licensed, or unreviewed source datasets. The `.gitignore` excludes common raw and generated data formats. Provenance and publishing permissions must be reviewed before sharing curated datasets.

An association score is not clinical evidence of antiviral efficacy. Missing drug–virus associations must not automatically be labeled true negatives.

See [the data-file inventory](docs/file_inventory.md) for where the existing files belong.
