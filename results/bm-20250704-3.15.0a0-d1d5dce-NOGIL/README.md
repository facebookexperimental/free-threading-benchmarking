# Results

- fork: python/d1d5dce14f90d777608e
- version: 3.15.0a0
- config: NOGIL
- commit hash: [d1d5dce](https://github.com/python/cpython/commit/d1d5dce)
- commit date: 2025-07-04T11:54:00-04:00
- commit merge base: [ade19880943509945da193202ca89e0b2b6fbd75](https://github.com/python/cpython/commit/ade19880943509945da193202ca89e0b2b6fbd75)
- ref: d1d5dce14f90d777608e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16082681115)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 95.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.md)
- [📈time plot](bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 95.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.md)
- [📈time plot](bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base-mem.svg)
- [📄table](bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base.md)
- [📈time plot](bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16082681115)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 97.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.md)
- [📈time plot](bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 74.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.md)
- [📈time plot](bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 83.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base-mem.svg)
- [📄table](bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base.md)
- [📈time plot](bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base.svg)

