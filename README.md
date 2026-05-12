# Evaluating Extraction-Based RAG: A Systematic Assessment of VerbatimRAG on the CLAPNQ Benchmark

This repository assesses [VerbatimRAG](https://github.com/KRLabsOrg/verbatim-rag) on the [CLAPNQ](https://github.com/primeqa/clapnq) benchmark, evaluating retrieval, extraction, and generation quality against generative baselines.

## Setup

Python 3.12

```bash
pip install -r requirements.txt
```

VerbatimRAG is included in `requirements.txt` and installed automatically from GitHub.

## Data

The following datasets are required but **not included** in this repository.

- **CLAPNQ** — [github.com/primeqa/clapnq](https://github.com/primeqa/clapnq)
  - `clapnq_dev_answerable.jsonl`
  - `clapnq_dev_unanswerable.jsonl`

Place all data files in a `data/` folder at the repo root.

## Structure

```
notebooks/
├── phase1/   # Automatic evaluation: retrieval, extraction, full RAG pipeline
├── phase2/   # Extraction evaluation against CLAPNQ sentence-level ground truth (IoU)
├── phase3/   # Sample selection and manual annotation of 100 examples
├── phase4/   # Qualitative comparison: VerbatimRAG vs. generative systems
```

## License

MIT
