# Results

- fork: python/fba5dded6df3c2b19435
- version: 3.15.0a0
- config: NOGIL
- commit hash: [fba5dde](https://github.com/python/cpython/commit/fba5dde)
- commit date: 2025-06-17T23:25:53+08:00
- commit merge base: [8dd8b5c2f0785675b9282b719256341448d49967](https://github.com/python/cpython/commit/8dd8b5c2f0785675b9282b719256341448d49967)
- ref: fba5dded6df3c2b19435

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15716179933)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde.json)

### vs. 3.12.6

- Geometric mean: 1.014x faster (HPT: reliability of 84.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde-vs-3.12.6.md)
- [📈time plot](bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x slower (HPT: reliability of 94.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde-vs-3.13.0rc2.md)
- [📈time plot](bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde-vs-3.13.0rc2.svg)

