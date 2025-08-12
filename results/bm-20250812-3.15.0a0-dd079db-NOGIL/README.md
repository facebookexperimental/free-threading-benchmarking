# Results

- fork: python/dd079db4b96fa474b8e6
- version: 3.15.0a0
- config: NOGIL
- commit hash: [dd079db](https://github.com/python/cpython/commit/dd079db)
- commit date: 2025-08-12T00:29:17+01:00
- commit merge base: [7140b99b0d0952167f7fdd747e6c28a8c8a2d768](https://github.com/python/cpython/commit/7140b99b0d0952167f7fdd747e6c28a8c8a2d768)
- ref: dd079db4b96fa474b8e6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16895596548)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250812-vultr-x86_64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 92.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250812-vultr-x86_64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-3.12.6.md)
- [📈time plot](bm-20250812-vultr-x86_64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 97.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250812-vultr-x86_64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-3.13.0rc2.md)
- [📈time plot](bm-20250812-vultr-x86_64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250812-vultr-x86_64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-base-mem.svg)
- [📄table](bm-20250812-vultr-x86_64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-base.md)
- [📈time plot](bm-20250812-vultr-x86_64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16895596548)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 94.05%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-3.12.6.md)
- [📈time plot](bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x slower (HPT: reliability of 85.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-3.13.0rc2.md)
- [📈time plot](bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.024x slower (HPT: reliability of 99.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-base-mem.svg)
- [📄table](bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-base.md)
- [📈time plot](bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db-vs-base.svg)

