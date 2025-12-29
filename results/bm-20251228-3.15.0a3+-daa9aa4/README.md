# Results

- fork: python/daa9aa4c0a8490f09b01
- version: 3.15.0a3+
- config: 
- commit hash: [daa9aa4](https://github.com/python/cpython/commit/daa9aa4)
- commit date: 2025-12-28T22:12:31+00:00
- commit merge base: [713684de5311eb9edb47f2f5fe3f4160f8d35e5a](https://github.com/python/cpython/commit/713684de5311eb9edb47f2f5fe3f4160f8d35e5a)
- ref: daa9aa4c0a8490f09b01

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20561802567)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251228-vultr-x86_64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251228-vultr-x86_64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-3.12.6.md)
- [📈time plot](bm-20251228-vultr-x86_64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251228-vultr-x86_64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-3.13.0rc2.md)
- [📈time plot](bm-20251228-vultr-x86_64-python-daa9aa4c0a8490f09b01-3.15.0a3%2B-daa9aa4-vs-3.13.0rc2.svg)

