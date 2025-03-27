# Results

- fork: python/898e6b395e63ad7f8bbe
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [898e6b3](https://github.com/python/cpython/commit/898e6b3)
- commit date: 2025-03-26T03:48:19Z
- commit merge base: [7bb41aef4b7b8f3c3f07c11b801c5b7f8afaac7f](https://github.com/python/cpython/commit/7bb41aef4b7b8f3c3f07c11b801c5b7f8afaac7f)
- ref: 898e6b395e63ad7f8bbe

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14109454219)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6%2B-898e6b3.json)

### vs. 3.12.6

- Geometric mean: 1.132x faster (HPT: reliability of 99.96%, 1.01x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6%2B-898e6b3-vs-3.12.6.md)
- [📈time plot](bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6%2B-898e6b3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 72.06%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6%2B-898e6b3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6%2B-898e6b3-vs-3.13.0rc2.svg)

