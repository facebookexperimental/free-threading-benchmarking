# Results

- fork: python/5d8e981c8477ce483374
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [5d8e981](https://github.com/python/cpython/commit/5d8e981)
- commit date: 2025-03-21T15:48:10+01:00
- commit merge base: [d3f6063af18a008e316e4342492e877ee51463e2](https://github.com/python/cpython/commit/d3f6063af18a008e316e4342492e877ee51463e2)
- ref: 5d8e981c8477ce483374

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14040042956)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250321-macm4pro-arm64-python-5d8e981c8477ce483374-3.14.0a6%2B-5d8e981.json)

### vs. 3.12.6

- Geometric mean: 1.068x slower (HPT: reliability of 99.96%, 1.04x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250321-macm4pro-arm64-python-5d8e981c8477ce483374-3.14.0a6%2B-5d8e981-vs-3.12.6.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-5d8e981c8477ce483374-3.14.0a6%2B-5d8e981-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.136x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250321-macm4pro-arm64-python-5d8e981c8477ce483374-3.14.0a6%2B-5d8e981-vs-3.13.0rc2.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-5d8e981c8477ce483374-3.14.0a6%2B-5d8e981-vs-3.13.0rc2.svg)

