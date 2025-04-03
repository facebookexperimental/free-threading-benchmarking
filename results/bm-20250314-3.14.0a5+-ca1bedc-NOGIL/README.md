# Results

- fork: python/ca1bedc9a4da523f4d1f
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [ca1bedc](https://github.com/python/cpython/commit/ca1bedc)
- commit date: 2025-03-14T16:25:56+02:00
- commit merge base: [db62557e3d1b0de4ca17786bd53f9c825ad88721](https://github.com/python/cpython/commit/db62557e3d1b0de4ca17786bd53f9c825ad88721)
- ref: ca1bedc9a4da523f4d1f

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14244921858)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5%2B-ca1bedc.json)

### vs. 3.12.6

- Geometric mean: 1.047x faster (HPT: reliability of 53.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5%2B-ca1bedc-vs-3.12.6.md)
- [📈time plot](bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5%2B-ca1bedc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x slower (HPT: reliability of 98.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5%2B-ca1bedc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5%2B-ca1bedc-vs-3.13.0rc2.svg)

