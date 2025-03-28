# Results

- fork: python/2c686a9ac243800b630d
- version: 3.14.0a6+
- config: 
- commit hash: [2c686a9](https://github.com/python/cpython/commit/2c686a9)
- commit date: 2025-03-26T18:44:56+00:00
- commit merge base: [67fbfb42bd5dfe861d0c58d9e6c48d8eef033d24](https://github.com/python/cpython/commit/67fbfb42bd5dfe861d0c58d9e6c48d8eef033d24)
- ref: 2c686a9ac243800b630d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14122854869)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250326-vultr-x86_64-python-2c686a9ac243800b630d-3.14.0a6%2B-2c686a9.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-vultr-x86_64-python-2c686a9ac243800b630d-3.14.0a6%2B-2c686a9-vs-3.12.6.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-2c686a9ac243800b630d-3.14.0a6%2B-2c686a9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 97.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-vultr-x86_64-python-2c686a9ac243800b630d-3.14.0a6%2B-2c686a9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-2c686a9ac243800b630d-3.14.0a6%2B-2c686a9-vs-3.13.0rc2.svg)

