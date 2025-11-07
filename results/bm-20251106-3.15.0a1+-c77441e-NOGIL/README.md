# Results

- fork: python/c77441ef1d1f3182280b
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [c77441e](https://github.com/python/cpython/commit/c77441e)
- commit date: 2025-11-06T16:02:47-08:00
- commit merge base: [42d014086098d3d70cacb4d8993f04cace120c12](https://github.com/python/cpython/commit/42d014086098d3d70cacb4d8993f04cace120c12)
- ref: c77441ef1d1f3182280b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19154149236)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251106-vultr-x86_64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e.json)

### vs. 3.12.6

- Geometric mean: 1.016x slower (HPT: reliability of 81.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251106-vultr-x86_64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-3.12.6.md)
- [📈time plot](bm-20251106-vultr-x86_64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x slower (HPT: reliability of 96.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251106-vultr-x86_64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251106-vultr-x86_64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251106-vultr-x86_64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-base-mem.svg)
- [📄table](bm-20251106-vultr-x86_64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-base.md)
- [📈time plot](bm-20251106-vultr-x86_64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19154149236)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251106-macm4pro-arm64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 99.75%, 1.01x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251106-macm4pro-arm64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-3.12.6.md)
- [📈time plot](bm-20251106-macm4pro-arm64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 55.02%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251106-macm4pro-arm64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251106-macm4pro-arm64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.036x slower (HPT: reliability of 99.98%, 1.01x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20251106-macm4pro-arm64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-base-mem.svg)
- [📄table](bm-20251106-macm4pro-arm64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-base.md)
- [📈time plot](bm-20251106-macm4pro-arm64-python-c77441ef1d1f3182280b-3.15.0a1%2B-c77441e-vs-base.svg)

