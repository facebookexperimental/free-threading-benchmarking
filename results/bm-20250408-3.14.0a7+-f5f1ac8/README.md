# Results

- fork: python/f5f1ac84b3b9d688b9e7
- version: 3.14.0a7+
- config: 
- commit hash: [f5f1ac8](https://github.com/python/cpython/commit/f5f1ac8)
- commit date: 2025-04-08T22:08:00+03:00
- commit merge base: [8421b648e91981e393a740dd9fb7b7dbf4cf07dc](https://github.com/python/cpython/commit/8421b648e91981e393a740dd9fb7b7dbf4cf07dc)
- ref: f5f1ac84b3b9d688b9e7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14345292525)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7%2B-f5f1ac8.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7%2B-f5f1ac8-vs-3.12.6.md)
- [📈time plot](bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7%2B-f5f1ac8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 92.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7%2B-f5f1ac8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7%2B-f5f1ac8-vs-3.13.0rc2.svg)

