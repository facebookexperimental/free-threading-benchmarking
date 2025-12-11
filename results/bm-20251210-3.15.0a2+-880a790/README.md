# Results

- fork: python/880a7905ca53d3c5c229
- version: 3.15.0a2+
- config: 
- commit hash: [880a790](https://github.com/python/cpython/commit/880a790)
- commit date: 2025-12-10T15:35:51-08:00
- commit merge base: [dc3ece2bc06d56c21ef81f86424b4598880ba1c8](https://github.com/python/cpython/commit/dc3ece2bc06d56c21ef81f86424b4598880ba1c8)
- ref: 880a7905ca53d3c5c229

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20117798572)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251210-vultr-x86_64-python-880a7905ca53d3c5c229-3.15.0a2%2B-880a790.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251210-vultr-x86_64-python-880a7905ca53d3c5c229-3.15.0a2%2B-880a790-vs-3.12.6.md)
- [📈time plot](bm-20251210-vultr-x86_64-python-880a7905ca53d3c5c229-3.15.0a2%2B-880a790-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251210-vultr-x86_64-python-880a7905ca53d3c5c229-3.15.0a2%2B-880a790-vs-3.13.0rc2.md)
- [📈time plot](bm-20251210-vultr-x86_64-python-880a7905ca53d3c5c229-3.15.0a2%2B-880a790-vs-3.13.0rc2.svg)

