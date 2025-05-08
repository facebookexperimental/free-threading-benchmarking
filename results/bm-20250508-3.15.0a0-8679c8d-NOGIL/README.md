# Results

- fork: python/8679c8d5ccf657835a88
- version: 3.15.0a0
- config: NOGIL
- commit hash: [8679c8d](https://github.com/python/cpython/commit/8679c8d)
- commit date: 2025-05-08T04:46:23+00:00
- commit merge base: [8598e57942f26ca1feecc0aefb421935e4e9f2aa](https://github.com/python/cpython/commit/8598e57942f26ca1feecc0aefb421935e4e9f2aa)
- ref: 8679c8d5ccf657835a88

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14900719235)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d.json)

### vs. 3.12.6

- Geometric mean: 1.014x faster (HPT: reliability of 89.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d-vs-3.12.6.md)
- [📈time plot](bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 96.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d-vs-3.13.0rc2.svg)

