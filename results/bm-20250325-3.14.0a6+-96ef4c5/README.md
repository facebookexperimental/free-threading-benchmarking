# Results

- fork: python/96ef4c511f3ec763dbb0
- version: 3.14.0a6+
- config: 
- commit hash: [96ef4c5](https://github.com/python/cpython/commit/96ef4c5)
- commit date: 2025-03-25T16:48:46+05:30
- commit merge base: [6fb5f7f4d9d22c49f5c29d2ffcbcc32b6cd7d06a](https://github.com/python/cpython/commit/6fb5f7f4d9d22c49f5c29d2ffcbcc32b6cd7d06a)
- ref: 96ef4c511f3ec763dbb0

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14264986933)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5.json)

### vs. 3.12.6

- Geometric mean: 1.065x faster (HPT: reliability of 99.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.12.6.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x slower (HPT: reliability of 95.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.13.0rc2.svg)

