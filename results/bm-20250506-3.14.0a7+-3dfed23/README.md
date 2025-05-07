# Results

- fork: python/3dfed230928de0f64906
- version: 3.14.0a7+
- config: 
- commit hash: [3dfed23](https://github.com/python/cpython/commit/3dfed23)
- commit date: 2025-05-06T15:05:20+03:00
- commit merge base: [f8691901d734388a776fe3b66a92ee1dcd11c2f1](https://github.com/python/cpython/commit/f8691901d734388a776fe3b66a92ee1dcd11c2f1)
- ref: 3dfed230928de0f64906

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14872386748)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.12.6.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 73.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.13.0rc2.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.13.0rc2.svg)

