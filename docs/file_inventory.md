# Existing file inventory and intended placement

The paths below are the intended local destinations for the files previously supplied for this project. The files themselves are not uploaded to this public repository by this scaffold.

| Supplied filename | Intended local destination | Purpose / status |
|---|---|---|
| Drug_HMPV(1).xlsx | data/raw/drugs/ | Drug catalogue source; inspect schema and provenance |
| Drugs(1).xlsx | data/raw/drugs/ | Original candidate-drug list |
| Drugs Revised (1)(1).xlsx | data/raw/drugs/ | Revised candidate-drug list; curate separately |
| Drugs (1) (1)(1).xlsx | data/raw/reference/ | Apparent duplicate candidate list; compare hashes/content |
| Viruses(1).xlsx | data/raw/viruses/ | Virus/accession source |
| Viruses (2)(1).xlsx | data/raw/reference/ | Virus taxonomy/reference workbook |
| Recommended_Viruses(1).xlsx | data/interim/virus_metadata/ | Recommended virus/segment metadata; validate |
| HANTA(1).txt | data/raw/viruses/ | Sequence source; inspect format before assigning .fasta extension |
| intraction_matrix_hmpv(1).csv | data/raw/interactions/ | Original drug-virus association matrix; validate IDs and labels |
| virus_proteins(1).csv | data/interim/virus_proteins/ | Protein records; validate virus-to-protein mapping |
| virus_proteins(1).fasta | data/interim/virus_proteins/ | Protein sequences; validate mapping and encoder input requirements |
| Drugs_info(1).csv | data/legacy/similarity_baseline/ | Previous RDKit/similarity workflow |
| Drugs_info_with_similarity_rdkit(1).csv | data/legacy/similarity_baseline/ | Previous RDKit/similarity workflow |
| drug_similarity_matrix_rdkit(1).csv | data/legacy/similarity_baseline/ | Previous similarity matrix |
| virus_ids(1).csv | data/legacy/previous_virus_embeddings/ | IDs corresponding to previous embedding artifact |
| virus_embeddings(1).npy | data/legacy/previous_virus_embeddings/ | Previous embeddings; validate model, dimensions and row order |
| virus_clusters(1).csv | data/legacy/previous_virus_embeddings/ | Previous clustering output |
| HMPV_Upgraded_Matrix_And_Audit(2).zip | data/processed/interactions/matrix_expansion_audit/ | Audit bundle; inspect before deriving training labels |

## Important validation gates

- Do not assume missing drug-virus associations are negative labels.
- Review the audit mask and provenance of all matrix cells before supervised learning.
- Resolve discrepancies in matrix row counts and duplicated virus identifiers.
- Confirm drug identity, SMILES, duplicate handling and the exclusion of peptide candidates from the current small-molecule scope.
- Confirm sequence identifiers, virus-to-segment/protein mapping, sequence format and encoder compatibility.
- Keep prior embeddings and similarity outputs isolated from the new MoLFormer/HViLM pipeline until provenance and compatibility are established.

The inventory records intended placement only. It does not certify file contents, correctness, licensing, or suitability for model training.
