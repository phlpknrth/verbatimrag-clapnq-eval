# Evaluating Extraction-Based RAG: A Systematic Assessment of VerbatimRAG on the CLAPNQ Benchmark

This repository assesses [VerbatimRAG](https://github.com/KRLabsOrg/verbatim-rag) on the [CLAPNQ](https://github.com/primeqa/clapnq) benchmark, evaluating retrieval, extraction, and generation quality against generative baselines.

## Setup

Python 3.12

```bash
pip install -r requirements.txt
```

VerbatimRAG is included in `requirements.txt` and installed automatically from GitHub.

Create a `.env` file at the repo root:
```
OPENAI_API_KEY=your_key_here
```

## Data

The following datasets are required but **not included** in this repository.

- **CLAPNQ** — [github.com/primeqa/clapnq](https://github.com/primeqa/clapnq)
  - `clapnq_dev_answerable.jsonl`
  - `clapnq_dev_unanswerable.jsonl`
 
- **HPO Paper results** (Orbach et al., 2025) — generation outputs used for qualitative comparison in Phase 4, available at [github.com/IBM/rag-hpo-bench](https://github.com/IBM/rag-hpo-bench)

Place all data files in a `data/` folder at the repo root.

## Structure

```
notebooks/
├── database_generation/   # Notebook for building Milvus vector database
├── phase1/   # Automatic evaluation: retrieval, extraction, full RAG pipeline
├── phase2/   # Extraction evaluation against CLAPNQ sentence-level ground truth
├── phase3/   # Annotation postprocessing
├── phase4/   # Re-evaluation on fine-grained self-annotated spans
```

## License

MIT
