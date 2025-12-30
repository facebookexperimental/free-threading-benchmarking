# Results

- fork: python/6cb245d26086369bb075
- version: 3.15.0a3+
- config: JIT
- commit hash: [6cb245d](https://github.com/python/cpython/commit/6cb245d)
- commit date: 2025-12-29T15:10:42Z
- commit merge base: [f37f57dfe683163f390ef589301e4dd4608c4288](https://github.com/python/cpython/commit/f37f57dfe683163f390ef589301e4dd4608c4288)
- ref: 6cb245d26086369bb075

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20586159393)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3%2B-6cb245d.json)

### vs. 3.12.6

- Geometric mean: 1.236x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3%2B-6cb245d-vs-3.12.6.md)
- [📈time plot](bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3%2B-6cb245d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.146x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3%2B-6cb245d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3%2B-6cb245d-vs-3.13.0rc2.svg)

