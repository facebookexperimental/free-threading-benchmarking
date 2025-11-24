# Results

- fork: python/425f24e4fad672c21130
- version: 3.15.0a2+
- config: 
- commit hash: [425f24e](https://github.com/python/cpython/commit/425f24e)
- commit date: 2025-11-23T15:37:15-08:00
- commit merge base: [23b67aa037cbb89b2a3d2c5fc716ca18f5b15b87](https://github.com/python/cpython/commit/23b67aa037cbb89b2a3d2c5fc716ca18f5b15b87)
- ref: 425f24e4fad672c21130

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19619725789)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e.json)

### vs. 3.12.6

- Geometric mean: 1.136x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.12.6.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 99.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.13.0rc2.svg)

