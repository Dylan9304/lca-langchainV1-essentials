# Start Here

Read this file first before making changes in this repo.

## Scope

- Primary work area: `python/`
- Main notebook: `python/L1_fast_agent.ipynb`
- Goal of the current setup: run the notebook with z.ai/Zhipu-compatible APIs, not OpenAI

## Current State

- `python/L1_fast_agent.ipynb` uses `langchain_openai.ChatOpenAI`
- Model: `glm-4.7`
- API base URL: `https://open.bigmodel.cn/api/paas/v4/`
- API key env var: `ZAI_API_KEY`
- `python/example.env` is aligned to `ZAI_API_KEY`
- Create your own local `python/.env` from `python/example.env`

## Resume Checklist

1. Change into `python/`
2. Use the existing local virtualenv if present: `.venv/`
3. Do not commit `.venv/`
4. Create `python/.env` from `python/example.env` if it does not exist
5. Load settings from `python/.env`
6. Re-run `python/L1_fast_agent.ipynb` from the top

## Notes

- If the notebook returns `429 Too Many Requests`, that is provider-side rate limiting, not an OpenAI issue.
- Do not commit `python/.env` to a public remote.
- If dependencies change, keep `python/pyproject.toml` and `python/uv.lock` in sync.
