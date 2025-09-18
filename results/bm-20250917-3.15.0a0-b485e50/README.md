# Results

- fork: python/b485e50fde3be08d796a
- version: 3.15.0a0
- config: 
- commit hash: [b485e50](https://github.com/python/cpython/commit/b485e50)
- commit date: 2025-09-17T16:50:15-05:00
- commit merge base: [5a15e7378996358848394930343e9633b6fec8a9](https://github.com/python/cpython/commit/5a15e7378996358848394930343e9633b6fec8a9)
- ref: b485e50fde3be08d796a

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17814204025)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50.json)

### vs. 3.12.6

- Geometric mean: 1.109x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50-vs-3.12.6.md)
- [📈time plot](bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 98.67%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50-vs-3.13.0rc2.md)
- [📈time plot](bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50-vs-3.13.0rc2.svg)

