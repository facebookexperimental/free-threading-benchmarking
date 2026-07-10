# Results

- fork: python/b2d8db1ac818e74ffe66
- version: 3.16.0a0
- config: NOGIL
- commit hash: [b2d8db1](https://github.com/python/cpython/commit/b2d8db1)
- commit date: 2026-07-09T00:17:05+01:00
- commit merge base: [0c6422ff6a13ae309493fb7a358cb35d7ea959c8](https://github.com/python/cpython/commit/0c6422ff6a13ae309493fb7a358cb35d7ea959c8)
- ref: b2d8db1ac818e74ffe66

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28986049512)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 84.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1-vs-3.12.6.md)
- [📈time plot](bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 97.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1-vs-3.13.0rc2.md)
- [📈time plot](bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1-vs-base-mem.svg)
- [📄table](bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1-vs-base.md)
- [📈time plot](bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1-vs-base.svg)

