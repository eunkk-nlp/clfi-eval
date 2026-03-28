# CLFI-Eval: Cross-Lingual Factual Inconsistency Evaluation Dataset

<!-- 
This repository contains the evaluation dataset used in the paper:

**"Measuring Multilingual Knowledge Asymmetry in Large Language Models:
An Empirical Analysis Across Languages and Domains"**
*Submitted to IEICE Transactions on Information and Systems (under review)*

-->


## Dataset

`dataset/queries.json` contains 422 factual queries across four knowledge
domains (person, geography, organization, statistics) and three languages
(Korean, Japanese, English), grounded in Wikidata triples.

## Format

Each entry includes:
- `id`: unique query identifier (e.g., `P-001`)
- `domain`: knowledge domain (`person`, `geography`, `organization`, `statistics`)
- `entity_id`: Wikidata entity identifier (e.g., `Q439722`)
- `entity_name_ko`: entity name in Korean
- `wikidata_property`: Wikidata property code (e.g., `P569`)
- `property_label`: property label in Korean (e.g., `출생연도`)
- `query`: query text in three languages (`ko`, `en`, `ja`)
- `answer_triple`: ground-truth answer in three languages plus Wikidata subject/predicate/object
- `answer_type`: answer type (`year`, `entity`, `numeric`)
- `numeric_tolerance`: tolerance threshold for numeric answers (null if not applicable)

## Notes

Model responses (GPT-4o-mini and Llama-3.1-8B outputs) are not 
included in this repository. GPT-4o-mini responses were obtained 
via the OpenAI API and cannot be redistributed under OpenAI's 
usage policies. Llama-3.1-8B responses were generated locally 
and are omitted to keep the repository lightweight.

Only the query dataset and ground-truth answers derived from 
Wikidata (CC0 license) are provided here.

## Citation
This dataset is associated with a paper currently under review.
Citation information will be added upon publication.

## License
- Dataset queries and ground-truth answers: derived from Wikidata (CC0 1.0)
- This repository: CC BY 4.0
