# Results

- fork: python/0eeaa0ef8bf60fd3b144
- version: 3.14.0a7+
- config: CLANG,NOGIL
- commit hash: [0eeaa0e](https://github.com/python/cpython/commit/0eeaa0e)
- commit date: 2025-05-05T13:48:09-04:00
- commit merge base: [4ac916ae33b962cb6b4f8849556403594b22a7f2](https://github.com/python/cpython/commit/4ac916ae33b962cb6b4f8849556403594b22a7f2)
- ref: 0eeaa0ef8bf60fd3b144

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14872001273)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e.json)

### vs. 3.12.6

- Geometric mean: 1.054x faster (HPT: reliability of 61.57%, 1.00x faster at 99th %ile)
- Memory usage: 1.46x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e-vs-3.12.6.md)
- [📈time plot](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 80.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.45x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e-vs-3.13.0rc2.svg)

