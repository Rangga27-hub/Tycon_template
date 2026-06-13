# Preset: ML PROJECT

> Default for `ml-project`. Tune to the task (classification/CV/NLP) in DECISIONS.md.

## Docs that apply for this type
Universal + **DATABASE.md (data & model section)**, optionally API.md (if serving), FEATURES.md.
NOT applicable: FRONTEND.md, DESIGN_DNA.md (unless a demo UI is built).
Type rules: create `rules/ml/` for reproducibility + data-contract rules.

## Stack
| Layer | Choice | Note |
|-------|--------|------|
| Language | Python 3.11+ | |
| Pkg manager | uv | faster than pip/conda |
| Classic ML | scikit-learn | baselines |
| Deep learning | PyTorch | when NN/CV/NLP |
| Data | pandas + polars | polars for big data |
| Notebook | Jupyter / Colab | exploration only |
| Schema | Pydantic | config & I/O |
| Serving | FastAPI | model API |
| Tracking | MLflow | experiments |
| Deploy | Hugging Face Spaces / Modal | demo & inference |

## Structure
```
data/{raw,processed}/
notebooks/          # exploration
src/{data,features,models,evaluation,api}/
models/             # saved artifacts
config/  tests/
pyproject.toml
```

## Type rules (reproducibility — strict)
- Set & record a random seed everywhere.
- Notebooks for exploration; production code moves to `src/`.
- Log dataset version, metrics, hyperparameters (DATABASE.md + MLflow).
- Separate config from code (Pydantic settings / yaml).
- Pin dependency versions; record data splits.

## Quick setup
```bash
pip install uv && uv venv && source .venv/bin/activate
uv pip install scikit-learn pandas polars torch fastapi uvicorn pydantic mlflow jupyter
```
