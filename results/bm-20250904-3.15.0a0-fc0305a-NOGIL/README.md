# Results

- fork: python/fc0305a2d8bef7cffaa4
- version: 3.15.0a0
- config: NOGIL
- commit hash: [fc0305a](https://github.com/python/cpython/commit/fc0305a)
- commit date: 2025-09-04T13:45:21-07:00
- commit merge base: [f070f54c5f4a42c7c61d1d5d3b8f3b7203b4a0fb](https://github.com/python/cpython/commit/f070f54c5f4a42c7c61d1d5d3b8f3b7203b4a0fb)
- ref: fc0305a2d8bef7cffaa4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17480103848)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 91.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.md)
- [📈time plot](bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 98.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base-mem.svg)
- [📄table](bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base.md)
- [📈time plot](bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17480103848)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 93.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.md)
- [📈time plot](bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x slower (HPT: reliability of 76.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 99.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base-mem.svg)
- [📄table](bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base.md)
- [📈time plot](bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base.svg)

