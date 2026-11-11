# GLM-5

Documentation repository for the GLM-5 large language model (744B parameters, 40B active, MoE architecture).

## Structure

- `README.md` / `README_zh.md` — Project overview (EN/CN)
- `example/ascend.md` — Ascend NPU deployment guide (SGLang, vLLM, xLLM)
- `resources/` — Images, logo, WeChat QR code
- `requirements.txt` — Python dependencies (transformers, pre-commit, accelerate)

## Linting

Pre-commit hooks: ruff (import sorting + formatting), typos, pymarkdown.

```shell
pre-commit run --all-files
```

## Notes

- No Python source code — this is a documentation-only repo
- Markdown uses inline HTML intentionally (badges, centered images)
- `example/ascend.md` has duplicate heading names by design (same sub-sections per framework)
