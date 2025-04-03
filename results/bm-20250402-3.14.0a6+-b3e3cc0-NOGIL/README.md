# Results

- fork: python/b3e3cc054c2c7718c0ad
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [b3e3cc0](https://github.com/python/cpython/commit/b3e3cc0)
- commit date: 2025-04-02T20:30:31-07:00
- commit merge base: [6bd96894269be4754a811fb8ea1e3b627a676562](https://github.com/python/cpython/commit/6bd96894269be4754a811fb8ea1e3b627a676562)
- ref: b3e3cc054c2c7718c0ad

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14242423029)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 92.24%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-3.12.6.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x faster (HPT: reliability of 79.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.055x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-base-mem.svg)
- [📄table](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-base.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.030x faster (HPT: reliability of 85.17%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- [📄table](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6%2B-b3e3cc0-vs-default_base_vs_NOGIL.svg)

