# Results

- fork: python/main
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [275056a](https://github.com/python/cpython/commit/275056a)
- commit date: 2025-04-03T09:40:37+01:00
- commit merge base: [b3e3cc054c2c7718c0ad7c4690f76716649a2588](https://github.com/python/cpython/commit/b3e3cc054c2c7718c0ad7c4690f76716649a2588)
- ref: main

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14242423029)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250403-macm4pro-arm64-python-main-3.14.0a6%2B-275056a.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 95.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250403-macm4pro-arm64-python-main-3.14.0a6%2B-275056a-vs-3.12.6.md)
- [📈time plot](bm-20250403-macm4pro-arm64-python-main-3.14.0a6%2B-275056a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x faster (HPT: reliability of 70.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250403-macm4pro-arm64-python-main-3.14.0a6%2B-275056a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250403-macm4pro-arm64-python-main-3.14.0a6%2B-275056a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250403-macm4pro-arm64-python-main-3.14.0a6%2B-275056a-vs-base-mem.svg)
- [📄table](bm-20250403-macm4pro-arm64-python-main-3.14.0a6%2B-275056a-vs-base.md)
- [📈time plot](bm-20250403-macm4pro-arm64-python-main-3.14.0a6%2B-275056a-vs-base.svg)

