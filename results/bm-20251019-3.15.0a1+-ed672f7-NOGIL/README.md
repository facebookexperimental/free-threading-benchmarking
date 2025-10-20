# Results

- fork: python/ed672f7a8a3c843d8e6e
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [ed672f7](https://github.com/python/cpython/commit/ed672f7)
- commit date: 2025-10-19T16:16:35-04:00
- commit merge base: [f9323213c98c9f1f7f3bf5af883b73047432fe50](https://github.com/python/cpython/commit/f9323213c98c9f1f7f3bf5af883b73047432fe50)
- ref: ed672f7a8a3c843d8e6e

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18638404683)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 98.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.12.6.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 64.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.13.0rc2.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 88.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-base-mem.svg)
- [📄table](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-base.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-base.svg)

