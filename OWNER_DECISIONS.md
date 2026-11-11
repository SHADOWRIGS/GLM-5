# Owner Decisions

## 1. MD024: Duplicate heading names in `example/ascend.md`

Headings "Single-node Deployment", "Multi-node Deployment", "Prefill-Decode Disaggregation" repeat
under SGLang/vLLM/xLLM sections. pymarkdown flags these as MD024. Options:

- **Keep as-is** (current) — readable, standard for deployment guides
- **Prefix headings** with framework name (e.g., "SGLang Single-node Deployment") — fixes lint but verbose

## 2. MD013: Line length in markdown files

Many lines exceed 80 chars (long URLs, descriptions). Options:

- **Keep as-is** — GitHub renders fine, no functional impact
- **Configure pymarkdown** to disable MD013 or raise the limit

## 3. MD033: Inline HTML in README files

`<div>`, `<br>`, `<p>`, `<img>` used for centered badges and logos. This is intentional and standard
for GitHub README files. Consider disabling MD033 in pymarkdown config if CI enforces it.

## 4. `==highlight==` syntax in `example/ascend.md`

Used throughout (`==GLM-5==`, `==vllm-ascend==`). This is non-standard markdown — rendered by some
parsers but not by GitHub. Consider replacing with backtick code spans or bold.
