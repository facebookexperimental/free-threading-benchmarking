# Results

- fork: python/0eeaa0ef8bf60fd3b144
- version: 3.14.0a7+
- config: CLANG
- commit hash: [0eeaa0e](https://github.com/python/cpython/commit/0eeaa0e)
- commit date: 2025-05-05T13:48:09-04:00
- commit merge base: [4ac916ae33b962cb6b4f8849556403594b22a7f2](https://github.com/python/cpython/commit/4ac916ae33b962cb6b4f8849556403594b22a7f2)
- ref: 0eeaa0ef8bf60fd3b144

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14872003342)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e.json)

### vs. 3.12.6

- Geometric mean: 1.141x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e-vs-3.12.6.md)
- [📈time plot](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7%2B-0eeaa0e-vs-3.13.0rc2.svg)

