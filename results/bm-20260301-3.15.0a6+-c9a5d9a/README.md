# Results

- fork: python/c9a5d9aae48a9faa553a
- version: 3.15.0a6+
- config: 
- commit hash: [c9a5d9a](https://github.com/python/cpython/commit/c9a5d9a)
- commit date: 2026-03-01T11:48:28-08:00
- commit merge base: [41fa2dbc0ef5232efae42630119ba20a2efb3ad7](https://github.com/python/cpython/commit/41fa2dbc0ef5232efae42630119ba20a2efb3ad7)
- ref: c9a5d9aae48a9faa553a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22556726564)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.md)
- [📈time plot](bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22556726564)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a.json)

### vs. 3.12.6

- Geometric mean: 1.169x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.md)
- [📈time plot](bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.svg)

