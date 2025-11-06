# Results

- fork: python/95f6e1275b1c9de550d9
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [95f6e12](https://github.com/python/cpython/commit/95f6e12)
- commit date: 2025-11-05T22:46:30Z
- commit merge base: [f0ab07f22c5fd18058a3ece7a1e745b3922af908](https://github.com/python/cpython/commit/f0ab07f22c5fd18058a3ece7a1e745b3922af908)
- ref: 95f6e1275b1c9de550d9

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19120676207)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251105-macm4pro-arm64-python-95f6e1275b1c9de550d9-3.15.0a1%2B-95f6e12.json)

### vs. 3.12.6

- Geometric mean: 1.095x faster (HPT: reliability of 99.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251105-macm4pro-arm64-python-95f6e1275b1c9de550d9-3.15.0a1%2B-95f6e12-vs-3.12.6.md)
- [📈time plot](bm-20251105-macm4pro-arm64-python-95f6e1275b1c9de550d9-3.15.0a1%2B-95f6e12-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x faster (HPT: reliability of 50.59%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251105-macm4pro-arm64-python-95f6e1275b1c9de550d9-3.15.0a1%2B-95f6e12-vs-3.13.0rc2.md)
- [📈time plot](bm-20251105-macm4pro-arm64-python-95f6e1275b1c9de550d9-3.15.0a1%2B-95f6e12-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.021x slower (HPT: reliability of 99.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20251105-macm4pro-arm64-python-95f6e1275b1c9de550d9-3.15.0a1%2B-95f6e12-vs-base-mem.svg)
- [📄table](bm-20251105-macm4pro-arm64-python-95f6e1275b1c9de550d9-3.15.0a1%2B-95f6e12-vs-base.md)
- [📈time plot](bm-20251105-macm4pro-arm64-python-95f6e1275b1c9de550d9-3.15.0a1%2B-95f6e12-vs-base.svg)

