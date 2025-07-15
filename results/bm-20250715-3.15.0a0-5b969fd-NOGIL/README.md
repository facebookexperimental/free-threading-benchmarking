# Results

- fork: python/5b969fd64502a6e2ba65
- version: 3.15.0a0
- config: NOGIL
- commit hash: [5b969fd](https://github.com/python/cpython/commit/5b969fd)
- commit date: 2025-07-15T11:56:42+02:00
- commit merge base: [c89a66feb12110e68e63a6293e3ed9c9fd180412](https://github.com/python/cpython/commit/c89a66feb12110e68e63a6293e3ed9c9fd180412)
- ref: 5b969fd64502a6e2ba65

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16295052533)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 94.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd-vs-3.12.6.md)
- [📈time plot](bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 96.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd-vs-3.13.0rc2.svg)

