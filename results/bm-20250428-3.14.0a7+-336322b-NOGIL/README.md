# Results

- fork: python/main
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [336322b](https://github.com/python/cpython/commit/336322b)
- commit date: 2025-04-28T20:18:56+01:00
- commit merge base: [606003ffa9e400cc22cc3b11f31118e2e24f688e](https://github.com/python/cpython/commit/606003ffa9e400cc22cc3b11f31118e2e24f688e)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14716471294)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250428-linux-x86_64-python-main-3.14.0a7%2B-336322b.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 87.91%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-linux-x86_64-python-main-3.14.0a7%2B-336322b-vs-3.12.6.md)
- [📈time plot](bm-20250428-linux-x86_64-python-main-3.14.0a7%2B-336322b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x faster (HPT: reliability of 57.61%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-linux-x86_64-python-main-3.14.0a7%2B-336322b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-linux-x86_64-python-main-3.14.0a7%2B-336322b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 88.59%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250428-linux-x86_64-python-main-3.14.0a7%2B-336322b-vs-base-mem.svg)
- [📄table](bm-20250428-linux-x86_64-python-main-3.14.0a7%2B-336322b-vs-base.md)
- [📈time plot](bm-20250428-linux-x86_64-python-main-3.14.0a7%2B-336322b-vs-base.svg)

