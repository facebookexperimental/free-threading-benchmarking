# Results

- fork: python/v3.14.0a6
- version: 3.14.0a6
- config: NOGIL
- commit hash: [77b2c93](https://github.com/python/cpython/commit/77b2c93)
- commit date: 2025-03-14T17:05:02+02:00
- commit merge base: [ca1bedc9a4da523f4d1f9c2ec92d98dcbed9c685](https://github.com/python/cpython/commit/ca1bedc9a4da523f4d1f9c2ec92d98dcbed9c685)
- ref: v3.14.0a6

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14244921858)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 99.86%, 1.01x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.12.6.md)
- [📈time plot](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.13.0rc2.md)
- [📈time plot](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.082x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-base-mem.svg)
- [📄table](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-base.md)
- [📈time plot](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-base.svg)

