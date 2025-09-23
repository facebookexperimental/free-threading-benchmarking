# Results

- fork: python/f0d8583303d28a5312e4
- version: 3.15.0a0
- config: 
- commit hash: [f0d8583](https://github.com/python/cpython/commit/f0d8583)
- commit date: 2025-09-22T09:34:02-07:00
- commit merge base: [04c4628345b841ae9792ea007d7beffd2846f017](https://github.com/python/cpython/commit/04c4628345b841ae9792ea007d7beffd2846f017)
- ref: f0d8583303d28a5312e4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17930090631)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583-vs-3.12.6.md)
- [📈time plot](bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583-vs-3.13.0rc2.md)
- [📈time plot](bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583-vs-3.13.0rc2.svg)

