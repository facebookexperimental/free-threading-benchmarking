# Results

- fork: Fidget-Spinner/resume_tracing
- version: 3.15.0a3+
- config: JIT
- commit hash: [9f28e87](https://github.com/Fidget%2dSpinner/cpython/commit/9f28e87)
- commit date: 2025-12-30T00:50:41Z
- commit merge base: [6cb245d26086369bb075858501405865fc255a10](https://github.com/python/cpython/commit/6cb245d26086369bb075858501405865fc255a10)
- ref: resume_tracing

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20586159393)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-9f28e87.json)

### vs. 3.12.6

- Geometric mean: 1.211x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, pycparser, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize
- [📄table](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-9f28e87-vs-3.12.6.md)
- [📈time plot](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-9f28e87-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.122x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, pycparser, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize
- [📄table](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-9f28e87-vs-3.13.0rc2.md)
- [📈time plot](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-9f28e87-vs-3.13.0rc2.svg)

