# Results

- fork: kumaraditya303/asyncio_perf
- version: 3.15.0a0
- config: NOGIL
- commit hash: [89e46c7](https://github.com/kumaraditya303/cpython/commit/89e46c7)
- commit date: 2025-07-15T17:24:29+05:30
- commit merge base: [5b969fd64502a6e2ba6513e2b18beaeae58b8aa1](https://github.com/python/cpython/commit/5b969fd64502a6e2ba6513e2b18beaeae58b8aa1)
- ref: asyncio_perf

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16295052533)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 91.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7-vs-3.12.6.md)
- [📈time plot](bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 96.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 99.19%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7-vs-base-mem.svg)
- [📄table](bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7-vs-base.md)
- [📈time plot](bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7-vs-base.svg)

