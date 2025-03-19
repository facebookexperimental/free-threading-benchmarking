# Results

- fork: python/f5e4c2955ba5977f468e
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [f5e4c29](https://github.com/python/cpython/commit/f5e4c29)
- commit date: 2025-03-19T14:42:51+01:00
- commit merge base: [8ad4646c675211dc1df0254a3160f50a18e4c6c3](https://github.com/python/cpython/commit/8ad4646c675211dc1df0254a3160f50a18e4c6c3)
- ref: f5e4c2955ba5977f468e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13948181749)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6%2B-f5e4c29.json)

### vs. 3.12.6

- Geometric mean: 1.045x faster (HPT: reliability of 55.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6%2B-f5e4c29-vs-3.12.6.md)
- [📈time plot](bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6%2B-f5e4c29-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 75.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6%2B-f5e4c29-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6%2B-f5e4c29-vs-3.13.0rc2.svg)

