# Results

- fork: python/v3.14.0a6
- version: 3.14.0a6
- config: 
- commit hash: [77b2c93](https://github.com/python/cpython/commit/77b2c93)
- commit date: 2025-03-14T17:05:02+02:00
- commit merge base: [ca1bedc9a4da523f4d1f9c2ec92d98dcbed9c685](https://github.com/python/cpython/commit/ca1bedc9a4da523f4d1f9c2ec92d98dcbed9c685)
- ref: v3.14.0a6

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13928899940)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json)

### vs. 3.12.6

- Geometric mean: 1.063x faster (HPT: reliability of 99.55%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.12.6.md)
- [📈time plot](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x slower (HPT: reliability of 96.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: chameleon, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.13.0rc2.md)
- [📈time plot](bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.13.0rc2.svg)

