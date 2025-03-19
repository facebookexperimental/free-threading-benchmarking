# Results

- fork: python/main
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [c1b42db](https://github.com/python/cpython/commit/c1b42db)
- commit date: 2025-03-18T16:28:00-05:00
- commit merge base: [f81990024554a75e2ab31133a72d9f0954690435](https://github.com/python/cpython/commit/f81990024554a75e2ab31133a72d9f0954690435)
- ref: main

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13934588318)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250318-vultr-x86_64-python-main-3.14.0a6%2B-c1b42db.json)

### vs. 3.12.6

- Geometric mean: 1.049x faster (HPT: reliability of 53.59%, 1.00x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-main-3.14.0a6%2B-c1b42db-vs-3.12.6.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-main-3.14.0a6%2B-c1b42db-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.015x faster (HPT: reliability of 79.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-main-3.14.0a6%2B-c1b42db-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-main-3.14.0a6%2B-c1b42db-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 99.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250318-vultr-x86_64-python-main-3.14.0a6%2B-c1b42db-vs-base-mem.svg)
- [📄table](bm-20250318-vultr-x86_64-python-main-3.14.0a6%2B-c1b42db-vs-base.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-main-3.14.0a6%2B-c1b42db-vs-base.svg)

