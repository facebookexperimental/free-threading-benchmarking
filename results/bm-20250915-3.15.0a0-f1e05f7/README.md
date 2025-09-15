# Results

- fork: DinoV/heap_ast_types
- version: 3.15.0a0
- config: 
- commit hash: [f1e05f7](https://github.com/DinoV/cpython/commit/f1e05f7)
- commit date: 2025-09-15T09:12:55-07:00
- commit merge base: [fa12c6bae47a41dd84e54b39d96bb73c4ba625c0](https://github.com/python/cpython/commit/fa12c6bae47a41dd84e54b39d96bb73c4ba625c0)
- ref: heap_ast_types

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17739668543)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7-vs-3.12.6.md)
- [📈time plot](bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 97.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7-vs-base-mem.svg)
- [📄table](bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7-vs-base.md)
- [📈time plot](bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7-vs-base.svg)

