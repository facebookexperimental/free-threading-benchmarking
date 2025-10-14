# Results

- fork: python/be60e4b4f34a097d999d
- version: 3.15.0a0
- config: 
- commit hash: [be60e4b](https://github.com/python/cpython/commit/be60e4b)
- commit date: 2025-10-13T13:10:39-07:00
- commit merge base: [c46265d94a2d2c5bcaabbbc312f8f6ac9162cd5f](https://github.com/python/cpython/commit/c46265d94a2d2c5bcaabbbc312f8f6ac9162cd5f)
- ref: be60e4b4f34a097d999d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18481686029)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251013-vultr-x86_64-python-be60e4b4f34a097d999d-3.15.0a0-be60e4b.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251013-vultr-x86_64-python-be60e4b4f34a097d999d-3.15.0a0-be60e4b-vs-3.12.6.md)
- [📈time plot](bm-20251013-vultr-x86_64-python-be60e4b4f34a097d999d-3.15.0a0-be60e4b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251013-vultr-x86_64-python-be60e4b4f34a097d999d-3.15.0a0-be60e4b-vs-3.13.0rc2.md)
- [📈time plot](bm-20251013-vultr-x86_64-python-be60e4b4f34a097d999d-3.15.0a0-be60e4b-vs-3.13.0rc2.svg)

