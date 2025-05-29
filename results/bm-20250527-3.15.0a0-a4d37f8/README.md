# Results

- fork: python/a4d37f88b66bc9a66b2a
- version: 3.15.0a0
- config: 
- commit hash: [a4d37f8](https://github.com/python/cpython/commit/a4d37f8)
- commit date: 2025-05-27T16:21:16-04:00
- commit merge base: [967f361993c9c97eb3ff3076a409b78ea32938df](https://github.com/python/cpython/commit/967f361993c9c97eb3ff3076a409b78ea32938df)
- ref: a4d37f88b66bc9a66b2a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15288579907)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250527-vultr-x86_64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250527-vultr-x86_64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8-vs-3.12.6.md)
- [📈time plot](bm-20250527-vultr-x86_64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250527-vultr-x86_64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250527-vultr-x86_64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15288579907)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8.json)

### vs. 3.12.6

- Geometric mean: 1.109x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8-vs-3.12.6.md)
- [📈time plot](bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 97.71%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8-vs-3.13.0rc2.svg)

