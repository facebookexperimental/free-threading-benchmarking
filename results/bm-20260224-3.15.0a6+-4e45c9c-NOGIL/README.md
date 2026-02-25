# Results

- fork: python/4e45c9c309abb12c6223
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [4e45c9c](https://github.com/python/cpython/commit/4e45c9c)
- commit date: 2026-02-24T22:52:02Z
- commit merge base: [5e61a16c1058e5de66b71dfdc9720d40e9f515d9](https://github.com/python/cpython/commit/5e61a16c1058e5de66b71dfdc9720d40e9f515d9)
- commit date: 2026-02-24T22:52:02+00:00
- ref: 4e45c9c309abb12c6223

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22376645023)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 75.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.md)
- [📈time plot](bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 87.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base-mem.svg)
- [📄table](bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base.md)
- [📈time plot](bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22376645023)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 99.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.md)
- [📈time plot](bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 60.82%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base-mem.svg)
- [📄table](bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base.md)
- [📈time plot](bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base.svg)

