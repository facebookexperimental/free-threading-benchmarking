# Results

- fork: nascheme/mcache_str_hash
- version: 3.15.0a0
- config: NOGIL
- commit hash: [b6bca55](https://github.com/nascheme/cpython/commit/b6bca55)
- commit date: 2025-05-08T00:03:52-07:00
- commit merge base: [8679c8d5ccf657835a88de5095d4fc6e2eb47633](https://github.com/python/cpython/commit/8679c8d5ccf657835a88de5095d4fc6e2eb47633)
- ref: mcache_str_hash

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14900719235)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 90.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55-vs-3.12.6.md)
- [📈time plot](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x slower (HPT: reliability of 98.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55-vs-3.13.0rc2.md)
- [📈time plot](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 97.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55-vs-base-mem.svg)
- [📄table](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55-vs-base.md)
- [📈time plot](bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55-vs-base.svg)

