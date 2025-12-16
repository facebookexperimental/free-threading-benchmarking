# Results

- fork: python/16a305f15242ed2acac9
- version: 3.15.0a3+
- config: CLANG,NOGIL
- commit hash: [16a305f](https://github.com/python/cpython/commit/16a305f)
- commit date: 2025-12-16T16:23:27+00:00
- commit merge base: [a0434075108efe6acdfba34f42545f4d80ac9a5e](https://github.com/python/cpython/commit/a0434075108efe6acdfba34f42545f4d80ac9a5e)
- ref: 16a305f15242ed2acac9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20282034234)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f.json)

### vs. 3.12.6

- Geometric mean: 1.026x faster (HPT: reliability of 95.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f-vs-3.12.6.md)
- [📈time plot](bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x slower (HPT: reliability of 54.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f-vs-3.13.0rc2.svg)

