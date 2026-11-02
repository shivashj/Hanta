# Methodology notes

## Planned representation pipeline

- Drug encoder: MoLFormer; planned embedding dimension 768.
- Virus encoder: HViLM candidate; planned embedding dimension 768.
- Encode sequence segments independently, then pool to a virus-level representation.
- Feed drug-virus embedding pairs to a neural-network predictor.

These are project design decisions, not evidence that embeddings or a trained model have already been produced.

## Required safeguards

1. Keep source data immutable.
2. Record source, retrieval date, license/permission, identifier mapping and transformation for each dataset.
3. Treat unknown/missing matrix entries as unknown, not automatically inactive.
4. Prevent leakage across train/validation/test splits, including related virus segments and duplicate drug/virus identifiers where applicable.
5. Report class balance, split strategy, metrics, uncertainty and limitations.
6. Do not interpret model scores as clinical efficacy.
