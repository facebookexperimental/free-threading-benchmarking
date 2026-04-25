# Results

- fork: python/95559d2a7e0071342dff
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [95559d2](https://github.com/python/cpython/commit/95559d2)
- commit date: 2026-04-24T11:22:05-07:00
- commit merge base: [665b7dfcfa240e02760f58bed5ca29ec01d028e6](https://github.com/python/cpython/commit/665b7dfcfa240e02760f58bed5ca29ec01d028e6)
- ref: 95559d2a7e0071342dff

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24918378286)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260424-vultr-x86_64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 58.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260424-vultr-x86_64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-3.12.6.md)
- [📈time plot](bm-20260424-vultr-x86_64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x slower (HPT: reliability of 83.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260424-vultr-x86_64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-3.13.0rc2.md)
- [📈time plot](bm-20260424-vultr-x86_64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260424-vultr-x86_64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-base-mem.svg)
- [📄table](bm-20260424-vultr-x86_64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-base.md)
- [📈time plot](bm-20260424-vultr-x86_64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24918378286)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260424-macm4pro-arm64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2.json)

### vs. 3.12.6

- Geometric mean: 1.112x faster (HPT: reliability of 99.90%, 1.02x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260424-macm4pro-arm64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-3.12.6.md)
- [📈time plot](bm-20260424-macm4pro-arm64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x faster (HPT: reliability of 71.62%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260424-macm4pro-arm64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-3.13.0rc2.md)
- [📈time plot](bm-20260424-macm4pro-arm64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.052x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260424-macm4pro-arm64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-base-mem.svg)
- [📄table](bm-20260424-macm4pro-arm64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-base.md)
- [📈time plot](bm-20260424-macm4pro-arm64-python-95559d2a7e0071342dff-3.15.0a8%2B-95559d2-vs-base.svg)

