# Results

- fork: python/06822bfbf625e9777813
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [06822bf](https://github.com/python/cpython/commit/06822bf)
- commit date: 2025-04-02T18:15:05Z
- commit merge base: [643dd5107cee995c0b48511bf5dbc52c695d11af](https://github.com/python/cpython/commit/643dd5107cee995c0b48511bf5dbc52c695d11af)
- ref: 06822bfbf625e9777813

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14245438897)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6%2B-06822bf.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 88.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6%2B-06822bf-vs-3.12.6.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6%2B-06822bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 83.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6%2B-06822bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6%2B-06822bf-vs-3.13.0rc2.svg)

