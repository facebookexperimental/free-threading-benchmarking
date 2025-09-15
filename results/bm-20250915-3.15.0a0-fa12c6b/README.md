# Results

- fork: python/fa12c6bae47a41dd84e5
- version: 3.15.0a0
- config: 
- commit hash: [fa12c6b](https://github.com/python/cpython/commit/fa12c6b)
- commit date: 2025-09-15T16:09:51+00:00
- commit merge base: [9c9a0f7da7bf626b6d156c9fe3df22597ee3fe9e](https://github.com/python/cpython/commit/9c9a0f7da7bf626b6d156c9fe3df22597ee3fe9e)
- ref: fa12c6bae47a41dd84e5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17739668543)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b-vs-3.12.6.md)
- [📈time plot](bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b-vs-3.13.0rc2.svg)

