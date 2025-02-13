# Results

- fork: DinoV/local_type_cache
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [1b02bc2](https://github.com/DinoV/cpython/commit/1b02bc2)
- commit date: 2025-02-12T17:23:21-08:00
- commit merge base: [1feaecc2bc42cb96f2d7bdc8d7083171bdcd0929](https://github.com/python/cpython/commit/1feaecc2bc42cb96f2d7bdc8d7083171bdcd0929)
- ref: local_type_cache

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13298377441)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2.json)

### vs. 3.12.6

- Geometric mean: 1.048x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-3.12.6.md)
- [📈time plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-3.13.0rc2.md)
- [📈time plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 95.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-base-mem.svg)
- [📄table](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-base.md)
- [📈time plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.134x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-1b02bc2-vs-default_base_vs_NOGIL.svg)

