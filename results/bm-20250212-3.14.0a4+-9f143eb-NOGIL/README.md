# Results

- fork: DinoV/local_type_cache
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [9f143eb](https://github.com/DinoV/cpython/commit/9f143eb)
- commit date: 2025-02-12T15:16:48-08:00
- commit merge base: [1feaecc2bc42cb96f2d7bdc8d7083171bdcd0929](https://github.com/python/cpython/commit/1feaecc2bc42cb96f2d7bdc8d7083171bdcd0929)
- ref: local_type_cache

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13296823968)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.96%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-3.12.6.md)
- [📈time plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 97.47%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-base-mem.svg)
- [📄table](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-base.md)
- [📈time plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.133x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4%2B-9f143eb-vs-default_base_vs_NOGIL.svg)

