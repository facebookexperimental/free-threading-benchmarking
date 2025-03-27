# Results

- fork: python/af29d5cfd19bf2656955
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [af29d5c](https://github.com/python/cpython/commit/af29d5c)
- commit date: 2025-03-24T10:14:22Z
- commit merge base: [491b8141f503743d88b69ff382a2be9eae4364e0](https://github.com/python/cpython/commit/491b8141f503743d88b69ff382a2be9eae4364e0)
- ref: af29d5cfd19bf2656955

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14095469048)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6%2B-af29d5c.json)

### vs. 3.12.6

- Geometric mean: 1.126x faster (HPT: reliability of 99.82%, 1.01x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6%2B-af29d5c-vs-3.12.6.md)
- [📈time plot](bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6%2B-af29d5c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 53.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6%2B-af29d5c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6%2B-af29d5c-vs-3.13.0rc2.svg)

