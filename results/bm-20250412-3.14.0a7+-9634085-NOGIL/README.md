# Results

- fork: python/9634085af3670b1eb654
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [9634085](https://github.com/python/cpython/commit/9634085)
- commit date: 2025-04-12T17:43:11+00:00
- commit merge base: [842ab815177549b9d4bec576d8f2c8f240b63506](https://github.com/python/cpython/commit/842ab815177549b9d4bec576d8f2c8f240b63506)
- ref: 9634085af3670b1eb654

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14422424640)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7%2B-9634085.json)

### vs. 3.12.6

- Geometric mean: 1.029x faster (HPT: reliability of 60.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7%2B-9634085-vs-3.12.6.md)
- [📈time plot](bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7%2B-9634085-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 93.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7%2B-9634085-vs-3.13.0rc2.md)
- [📈time plot](bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7%2B-9634085-vs-3.13.0rc2.svg)

