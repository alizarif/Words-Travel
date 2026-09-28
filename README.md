# Words Travel: The Global Transmission of Central Bank Language

## Files

- **01_scoring.ipynb** contains the text preparation, lexical scoring, LLM calls, embeddings, phrase matching, and reconstruction checks. Scoring is disabled by default because the completed outputs are supplied.
- **scoring_output.zip** contains only the saved measurements needed for the analysis. Leave it zipped.
- **02_analysis.ipynb** calculates the results and displays each table and figure in manuscript order. It also saves eleven table CSVs and six figure PDFs in a new `results/` folder.

## Saved measurements

The ZIP contains seven CSV files, with no subfolders.

| File | Contents |
|---|---|
| `statements.csv` | Statement dates, country information, document lengths, screening flags, and lexical and embedding scores. |
| `ratings.csv` | Two LLM ratings per statement and concept, including intensity, coverage, and quotation-verification flags. |
| `pair_ratings.csv` | Two LLM comparisons of each consecutive Fed statement pair. |
| `claims.csv` | Extracted claim categories and evidence-verification flags. |
| `phrase_overlap.csv` | Counts of new Fed phrases and matches in foreign statements, used to calculate phrase-match shares. |
| `reconstruction.csv` | Original and recovered ratings used to assess reconstruction accuracy. |
| `reconstruction_targets.csv` | Recovered ratings for the fixed target scores of 10, 50, and 90. |

The ZIP contains no statement texts, evidence quotations, or phrase strings.

Keep both notebooks and the ZIP together. The notebook handles the ZIP automatically.

## Regenerate the scores only if needed

Request the restricted statement texts from the [MPSD team](https://centralbanktexts.github.io/contact.html), then follow the instructions in `01_scoring.ipynb`. Regeneration requires API access and makes paid model calls. It is not needed to reproduce the supplied results.
