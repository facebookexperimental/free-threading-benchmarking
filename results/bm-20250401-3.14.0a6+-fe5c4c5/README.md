# Results

- fork: python/fe5c4c53e7bc6d780686
- version: 3.14.0a6+
- config: 
- commit hash: [fe5c4c5](https://github.com/python/cpython/commit/fe5c4c5)
- commit date: 2025-04-01T08:46:29+08:00
- commit merge base: [45a3ab5a81769eadd94da3e26eb9bb2f3ae80fb1](https://github.com/python/cpython/commit/45a3ab5a81769eadd94da3e26eb9bb2f3ae80fb1)
- ref: fe5c4c53e7bc6d780686

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14204760831)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.12.6.md)
- [📈time plot](bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 90.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base-mem.svg)
- [📄table](bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base.md)
- [📈time plot](bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base.svg)

