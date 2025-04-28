# Results

- fork: python/main
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [b739ec5](https://github.com/python/cpython/commit/b739ec5)
- commit date: 2025-04-28T19:09:28+03:00
- commit merge base: [58567cc18c5b048e08307b5ba18a9934a395ca42](https://github.com/python/cpython/commit/58567cc18c5b048e08307b5ba18a9934a395ca42)
- ref: main

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14714382434)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 87.28%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-3.12.6.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 92.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 98.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-base-mem.svg)
- [📄table](bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-base.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-base.svg)

