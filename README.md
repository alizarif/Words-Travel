# Words Travel: The Global Transmission of Central Bank Language

# Replication files

- **01_scoring.ipynb** prepares the texts and generates lexical scores, LLM ratings, and embedding scores. Saved outputs are provided, so scoring does not need to be repeated.
- **02_analysis.ipynb** uses the saved outputs to reproduce the main paper and appendix results, tables, and figures in order.

## Data archives

- **data/raw_data.zip** is not included in the distributed package because the underlying texts are restricted. Request access from the [Monetary Policy Statement Database team](https://centralbanktexts.github.io/contact.html).
- **data/scored_data.zip** contains the prepared analysis inputs, saved scores and annotations, supporting datasets, and scoring checks.
- **data/analysis_outputs.zip** contains the resulting estimates, table data, and verification reports.

## Inside scored_data.zip

### data/ — Reference material and supporting datasets

Contains the reference sentences used for scoring, benchmark scores and annotations, source-language classifications, and supplementary economic and financial data.

- **benchmark/** contains benchmark scores and LLM annotations.
- **external/** contains supporting datasets.
- **external/ecb_intro/** contains ECB introductory statements.
- **external/fed_minutes/** contains Federal Reserve minutes.

### audit/ — Records used to check the scoring process

Contains document-screening records, duplicate and date checks, changes between consecutive statements, candidate new phrases, model-request usage, scoring completion and failure records, and reconstruction diagnostics.

These files document how the inputs and scores were checked.

### derived/ — Prepared inputs for the analysis notebook

Contains the cleaned statement corpus, lexical and embedding scores, direct and pairwise LLM annotations, phrase classifications, and reconstructed statements.

These are the saved outputs from the scoring stage that support the empirical analysis.

### manifest.json — File inventory

Lists the archive’s files and their checksums for integrity verification.

## Text availability

The current `scored_data.zip` also contains cleaned MPSD statement texts in `derived/corpus.jsonl`. Excluding `raw_data.zip` therefore does not remove the underlying texts from the package. Public distribution requires resolving access restrictions for these copies as well.

Keep the folder structure unchanged. The notebooks handle the ZIP files automatically.
