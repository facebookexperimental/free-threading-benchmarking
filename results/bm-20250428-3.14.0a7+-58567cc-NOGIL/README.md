# Results

- fork: python/58567cc18c5b048e0830
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [58567cc](https://github.com/python/cpython/commit/58567cc)
- commit date: 2025-04-28T08:38:56-07:00
- commit merge base: [7f16f1bc114ea42ceb51ccb5008b74571a875f6b](https://github.com/python/cpython/commit/7f16f1bc114ea42ceb51ccb5008b74571a875f6b)
- ref: 58567cc18c5b048e0830

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14714382434)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc.json)

### vs. 3.12.6

- Geometric mean: 1.081x faster (HPT: reliability of 86.57%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc-vs-3.12.6.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 92.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc-vs-3.13.0rc2.svg)

