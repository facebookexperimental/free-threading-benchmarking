# Results

- fork: nascheme/mcache_str_hash
- version: 3.15.0a0
- config: NOGIL
- commit hash: [8335fa1](https://github.com/nascheme/cpython/commit/8335fa1)
- commit date: 2025-05-08T12:27:32-07:00
- commit merge base: [9546eeea90c8deb8570a0ef621f075c3c766bc12](https://github.com/python/cpython/commit/9546eeea90c8deb8570a0ef621f075c3c766bc12)
- ref: mcache_str_hash

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14915072017)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1.json)

### vs. 3.12.6

- Geometric mean: 1.008x faster (HPT: reliability of 90.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1-vs-3.12.6.md)
- [📈time plot](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x slower (HPT: reliability of 95.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 99.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1-vs-base-mem.svg)
- [📄table](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1-vs-base.md)
- [📈time plot](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1-vs-base.svg)

