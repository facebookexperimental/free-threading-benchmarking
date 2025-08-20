# Results

- fork: python/d22a7456443415961b93
- version: 3.15.0a0
- config: 
- commit hash: [d22a745](https://github.com/python/cpython/commit/d22a745)
- commit date: 2025-08-19T22:30:59+01:00
- commit merge base: [7d06a0af1720e1962b324d8abf5865121ca492bc](https://github.com/python/cpython/commit/7d06a0af1720e1962b324d8abf5865121ca492bc)
- ref: d22a7456443415961b93

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17085087684)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.12.6.md)
- [📈time plot](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.13.0rc2.md)
- [📈time plot](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17085087684)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.12.6.md)
- [📈time plot](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 71.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.13.0rc2.md)
- [📈time plot](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.13.0rc2.svg)

