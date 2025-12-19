### Setup

```bash
uv venv --python 3.10
source .venv/bin/activate
uv pip install -e .
python -m ipykernel install --user --name llm-uv310 --display-name "LLM (uv, py3.10)"
jupyter notebook
