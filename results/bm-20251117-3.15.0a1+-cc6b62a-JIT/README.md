# Results

- fork: python/main
- version: 3.15.0a1+
- config: JIT
- commit hash: [cc6b62a](https://github.com/python/cpython/commit/cc6b62a)
- commit date: 2025-11-17T14:51:21Z
- commit merge base: [3d148059479b28a21f8eae6abf6d1bcc91ab8cbb](https://github.com/python/cpython/commit/3d148059479b28a21f8eae6abf6d1bcc91ab8cbb)
- ref: main

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19434620332)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a.json)

### vs. 3.12.6

- Geometric mean: 1.138x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a-vs-3.12.6.md)
- [📈time plot](bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 99.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a-vs-3.13.0rc2.svg)

