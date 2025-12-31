# Results

- fork: Fidget-Spinner/resume_tracing
- version: 3.15.0a3+
- config: JIT
- commit hash: [d52a106](https://github.com/Fidget%2dSpinner/cpython/commit/d52a106)
- commit date: 2025-12-30T18:17:52Z
- commit merge base: [6cb245d26086369bb075858501405865fc255a10](https://github.com/python/cpython/commit/6cb245d26086369bb075858501405865fc255a10)
- ref: resume_tracing

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20603135539)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-d52a106.json)

### vs. 3.12.6

- Geometric mean: 1.261x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, docutils, gevent_hub, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sympy_expand, sympy_integrate, sympy_str, sympy_sum, tornado_http
- new benchmarks: sqlglot_v2_optimize, sqlglot_v2_parse
- [📄table](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-d52a106-vs-3.12.6.md)
- [📈time plot](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-d52a106-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.169x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, docutils, gevent_hub, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sympy_expand, sympy_integrate, sympy_str, sympy_sum, tornado_http
- new benchmarks: sqlglot_v2_optimize, sqlglot_v2_parse
- [📄table](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-d52a106-vs-3.13.0rc2.md)
- [📈time plot](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-d52a106-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 89.20%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: 🔴 docutils, pylint, sqlglot_v2_normalize, sqlglot_v2_transpile, sympy_expand, sympy_integrate, sympy_str, sympy_sum
- new benchmarks: asyncio_websockets
- [🧠memory plot](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-d52a106-vs-base-mem.svg)
- [📄table](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-d52a106-vs-base.md)
- [📈time plot](bm-20251230-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-d52a106-vs-base.svg)

