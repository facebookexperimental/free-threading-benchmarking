# Results

- fork: python/1391ee664c8f019996e0
- version: 3.15.0a3+
- config: 
- commit hash: [1391ee6](https://github.com/python/cpython/commit/1391ee6)
- commit date: 2025-12-18T21:29:54+00:00
- commit merge base: [e79c39101a9f55882f54df0bb3ecfa23238692de](https://github.com/python/cpython/commit/e79c39101a9f55882f54df0bb3ecfa23238692de)
- ref: 1391ee664c8f019996e0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20355697531)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.12.6.md)
- [📈time plot](bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.13.0rc2.md)
- [📈time plot](bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.13.0rc2.svg)

