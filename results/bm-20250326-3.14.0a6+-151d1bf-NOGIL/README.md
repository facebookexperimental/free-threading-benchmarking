# Results

- fork: python/151d1bfd1bb7ca9a36bb
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [151d1bf](https://github.com/python/cpython/commit/151d1bf)
- commit date: 2025-03-26T18:36:04-04:00
- commit merge base: [52b5eb95b770fa00ebbd449ba40cab4a0e7c7df7](https://github.com/python/cpython/commit/52b5eb95b770fa00ebbd449ba40cab4a0e7c7df7)
- ref: 151d1bfd1bb7ca9a36bb

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14096104884)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf.json)

### vs. 3.12.6

- Geometric mean: 1.065x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.12.6.md)
- [📈time plot](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.132x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base-mem.svg)
- [📄table](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base.md)
- [📈time plot](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base.svg)

