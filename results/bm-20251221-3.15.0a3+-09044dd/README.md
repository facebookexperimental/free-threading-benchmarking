# Results

- fork: python/09044dd42b50e628b197
- version: 3.15.0a3+
- config: 
- commit hash: [09044dd](https://github.com/python/cpython/commit/09044dd)
- commit date: 2025-12-21T08:58:07-08:00
- commit merge base: [b8d3fddba6e96e693ced0d3b8f6ddbd61428fd32](https://github.com/python/cpython/commit/b8d3fddba6e96e693ced0d3b8f6ddbd61428fd32)
- ref: 09044dd42b50e628b197

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20418248772)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251221-vultr-x86_64-python-09044dd42b50e628b197-3.15.0a3%2B-09044dd.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251221-vultr-x86_64-python-09044dd42b50e628b197-3.15.0a3%2B-09044dd-vs-3.12.6.md)
- [📈time plot](bm-20251221-vultr-x86_64-python-09044dd42b50e628b197-3.15.0a3%2B-09044dd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251221-vultr-x86_64-python-09044dd42b50e628b197-3.15.0a3%2B-09044dd-vs-3.13.0rc2.md)
- [📈time plot](bm-20251221-vultr-x86_64-python-09044dd42b50e628b197-3.15.0a3%2B-09044dd-vs-3.13.0rc2.svg)

