# Results

- fork: Fidget-Spinner/resume_tracing
- version: 3.15.0a3+
- config: JIT
- commit hash: [2e5e9e6](https://github.com/Fidget%2dSpinner/cpython/commit/2e5e9e6)
- commit date: 2025-12-31T00:19:45Z
- commit merge base: [6cb245d26086369bb075858501405865fc255a10](https://github.com/python/cpython/commit/6cb245d26086369bb075858501405865fc255a10)
- ref: resume_tracing

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20608885667)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-2e5e9e6.json)

### vs. 3.12.6

- Geometric mean: 1.226x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-2e5e9e6-vs-3.12.6.md)
- [📈time plot](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-2e5e9e6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.136x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-2e5e9e6-vs-3.13.0rc2.md)
- [📈time plot](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-2e5e9e6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 96.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-2e5e9e6-vs-base-mem.svg)
- [📄table](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-2e5e9e6-vs-base.md)
- [📈time plot](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-2e5e9e6-vs-base.svg)

