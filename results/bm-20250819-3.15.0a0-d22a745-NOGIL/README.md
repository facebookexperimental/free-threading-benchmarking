# Results

- fork: python/d22a7456443415961b93
- version: 3.15.0a0
- config: NOGIL
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

- Geometric mean: 1.028x slower (HPT: reliability of 93.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.12.6.md)
- [📈time plot](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 98.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.13.0rc2.md)
- [📈time plot](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-base-mem.svg)
- [📄table](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-base.md)
- [📈time plot](bm-20250819-vultr-x86_64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17085087684)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 93.46%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.12.6.md)
- [📈time plot](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x slower (HPT: reliability of 79.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.13.0rc2.md)
- [📈time plot](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 96.30%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-base-mem.svg)
- [📄table](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-base.md)
- [📈time plot](bm-20250819-macm4pro-arm64-python-d22a7456443415961b93-3.15.0a0-d22a745-vs-base.svg)

