# CLFI-Eval: Cross-Lingual Factual Inconsistency Evaluation Dataset

This repository contains the evaluation dataset used in the paper:

**"Measuring Multilingual Knowledge Asymmetry in Large Language Models:
An Empirical Analysis Across Languages and Domains"**
*Submitted to IEICE Transactions on Information and Systems (under review)*

## Dataset

`dataset/queries.json` contains 422 factual queries across four knowledge
domains (person, geography, organization, statistics) and three languages
(Japanese, Korean, English), grounded in Wikidata triples.

## Format

Each entry includes:
- `query_id`: unique identifier
- `domain`: knowledge domain
- `entity_name`: entity in each language
- `property`: Wikidata property (e.g., P569)
- `answer`: ground-truth answer
- `queries`: query text in Japanese, Korean, and English

## License
CC BY 4.0
