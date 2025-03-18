# Results

- fork: python/a936af924efc6e2fb59e
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [a936af9](https://github.com/python/cpython/commit/a936af9)
- commit date: 2025-03-17T18:34:37-04:00
- commit merge base: [f48887fb97651c02c5e412a75ed8b51a4ca11e6a](https://github.com/python/cpython/commit/f48887fb97651c02c5e412a75ed8b51a4ca11e6a)
- ref: a936af924efc6e2fb59e

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13912590604)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9.json)

### vs. 3.12.6

- Geometric mean: 1.009x slower (HPT: reliability of 98.35%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)
- [📈time plot](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg)

### vs. base

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: 🔴 dask, sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base-mem.svg)
- [📄table](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base.md)
- [📈time plot](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base.svg)

