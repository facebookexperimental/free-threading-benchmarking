# Results

- fork: python/726e8e8defc487c55ade
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [726e8e8](https://github.com/python/cpython/commit/726e8e8)
- commit date: 2025-12-08T21:10:48+00:00
- commit merge base: [719d7960e2b55ab8310df3d9d69b7c9df3283fbf](https://github.com/python/cpython/commit/719d7960e2b55ab8310df3d9d69b7c9df3283fbf)
- ref: 726e8e8defc487c55ade

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20047552401)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2%2B-726e8e8.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 91.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2%2B-726e8e8-vs-3.12.6.md)
- [📈time plot](bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2%2B-726e8e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x slower (HPT: reliability of 96.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2%2B-726e8e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2%2B-726e8e8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2%2B-726e8e8-vs-base-mem.svg)
- [📄table](bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2%2B-726e8e8-vs-base.md)
- [📈time plot](bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2%2B-726e8e8-vs-base.svg)

