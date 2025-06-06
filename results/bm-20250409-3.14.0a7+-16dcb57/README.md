# Results

- fork: python/16dcb576f7623e19f22b
- version: 3.14.0a7+
- config: 
- commit hash: [16dcb57](https://github.com/python/cpython/commit/16dcb57)
- commit date: 2025-04-09T01:01:36+02:00
- commit merge base: [f5f1ac84b3b9d688b9e7d5943c975904b6b74513](https://github.com/python/cpython/commit/f5f1ac84b3b9d688b9e7d5943c975904b6b74513)
- ref: 16dcb576f7623e19f22b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14346206557)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250409-vultr-x86_64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250409-vultr-x86_64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-3.12.6.md)
- [📈time plot](bm-20250409-vultr-x86_64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 94.08%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250409-vultr-x86_64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-3.13.0rc2.md)
- [📈time plot](bm-20250409-vultr-x86_64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 75.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250409-vultr-x86_64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-base-mem.svg)
- [📄table](bm-20250409-vultr-x86_64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-base.md)
- [📈time plot](bm-20250409-vultr-x86_64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14346206557)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250409-macm4pro-arm64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250409-macm4pro-arm64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-3.12.6.md)
- [📈time plot](bm-20250409-macm4pro-arm64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 54.29%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250409-macm4pro-arm64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-3.13.0rc2.md)
- [📈time plot](bm-20250409-macm4pro-arm64-python-16dcb576f7623e19f22b-3.14.0a7%2B-16dcb57-vs-3.13.0rc2.svg)

