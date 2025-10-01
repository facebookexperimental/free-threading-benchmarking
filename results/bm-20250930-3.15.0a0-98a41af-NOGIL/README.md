# Results

- fork: python/98a41af5b09343fa030e
- version: 3.15.0a0
- config: NOGIL
- commit hash: [98a41af](https://github.com/python/cpython/commit/98a41af)
- commit date: 2025-09-30T18:18:13Z
- commit merge base: [c86eb4d3ac5984efc1ea920ba643e3c4f02fdee8](https://github.com/python/cpython/commit/c86eb4d3ac5984efc1ea920ba643e3c4f02fdee8)
- commit date: 2025-09-30T18:18:13+00:00
- ref: 98a41af5b09343fa030e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18147276715)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 79.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.md)
- [📈time plot](bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x slower (HPT: reliability of 95.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.md)
- [📈time plot](bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base-mem.svg)
- [📄table](bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base.md)
- [📈time plot](bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18147276715)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 97.25%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.md)
- [📈time plot](bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x faster (HPT: reliability of 66.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.md)
- [📈time plot](bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x slower (HPT: reliability of 94.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base-mem.svg)
- [📄table](bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base.md)
- [📈time plot](bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base.svg)

