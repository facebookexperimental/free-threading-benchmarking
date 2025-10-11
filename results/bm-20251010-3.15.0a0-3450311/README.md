# Results

- fork: python/34503111fe2724986701
- version: 3.15.0a0
- config: 
- commit hash: [3450311](https://github.com/python/cpython/commit/3450311)
- commit date: 2025-10-10T06:36:40+08:00
- commit merge base: [f575dd9ef815e79cb359f5466375363f0a5756ca](https://github.com/python/cpython/commit/f575dd9ef815e79cb359f5466375363f0a5756ca)
- ref: 34503111fe2724986701

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18392751251)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.md)
- [📈time plot](bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.md)
- [📈time plot](bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.svg)

