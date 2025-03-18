# Results

- fork: python/v3.14.0a5
- version: 3.14.0a5
- config: NOGIL
- commit hash: [3ae9101](https://github.com/python/cpython/commit/3ae9101)
- commit date: 2025-02-11T19:16:29+02:00
- commit merge base: [5cdd6e5e758a3fc0a5daac80753bf611b3e23c2d](https://github.com/python/cpython/commit/5cdd6e5e758a3fc0a5daac80753bf611b3e23c2d)
- ref: v3.14.0a5

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13922087518)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json)

### vs. 3.12.6

- Geometric mean: 1.010x slower (HPT: reliability of 99.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.12.6.md)
- [📈time plot](bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.13.0rc2.md)
- [📈time plot](bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.13.0rc2.svg)

