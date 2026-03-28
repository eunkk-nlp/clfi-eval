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
(Japanese, Korean, English), grounded in Wikidata triples.

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

## License
CC BY 4.0
