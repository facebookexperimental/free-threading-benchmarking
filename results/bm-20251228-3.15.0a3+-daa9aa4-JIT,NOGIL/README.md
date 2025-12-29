# Results

- fork: python/daa9aa4c0a8490f09b01
- version: 3.15.0a3+
- config: JIT,NOGIL
- commit hash: [daa9aa4](https://github.com/python/cpython/commit/daa9aa4)
- commit date: 2025-12-28T22:12:31Z
- commit merge base: [713684de5311eb9edb47f2f5fe3f4160f8d35e5a](https://github.com/python/cpython/commit/713684de5311eb9edb47f2f5fe3f4160f8d35e5a)
- ref: daa9aa4c0a8490f09b01

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20561353582)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 91.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-3.12.6.md)
- [📈time plot](bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 86.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-3.13.0rc2.md)
- [📈time plot](bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.076x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-base-mem.svg)
- [📄table](bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-base.md)
- [📈time plot](bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-base.svg)

