# Results

- fork: python/3a8cefba0b60bd25c6b1
- version: 3.14.0a6+
- config: 
- commit hash: [3a8cefb](https://github.com/python/cpython/commit/3a8cefb)
- commit date: 2025-04-01T16:55:05-07:00
- commit merge base: [1a9d4a1fb3d4beda7c7e8483af7c6bc7ac477e9f](https://github.com/python/cpython/commit/1a9d4a1fb3d4beda7c7e8483af7c6bc7ac477e9f)
- ref: 3a8cefba0b60bd25c6b1

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14208761861)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb.json)

### vs. 3.12.6

- Geometric mean: 1.105x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.md)
- [📈time plot](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 78.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.svg)

