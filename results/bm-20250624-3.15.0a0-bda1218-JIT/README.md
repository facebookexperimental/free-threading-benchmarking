# Results

- fork: python/bda121862e7d7f4684d9
- version: 3.15.0a0
- config: JIT
- commit hash: [bda1218](https://github.com/python/cpython/commit/bda1218)
- commit date: 2025-06-24T03:42:09+08:00
- commit merge base: [569fc6870f048cb75469ae3cacb6ebcf5172a10e](https://github.com/python/cpython/commit/569fc6870f048cb75469ae3cacb6ebcf5172a10e)
- ref: bda121862e7d7f4684d9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16031600110)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218.json)

### vs. 3.12.6

- Geometric mean: 1.113x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218-vs-3.12.6.md)
- [📈time plot](bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218-vs-3.13.0rc2.md)
- [📈time plot](bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218-vs-3.13.0rc2.svg)

