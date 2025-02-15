# Results

- fork: DinoV/noclock_clear
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [c00cd86](https://github.com/DinoV/cpython/commit/c00cd86)
- commit date: 2025-02-14T13:40:32-08:00
- commit merge base: [39cd9728a6770d8fe7937c57385cda5c2e25a223](https://github.com/python/cpython/commit/39cd9728a6770d8fe7937c57385cda5c2e25a223)
- ref: noclock_clear

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13338001011)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-3.12.6.md)
- [📈time plot](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-3.13.0rc2.md)
- [📈time plot](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x faster (HPT: reliability of 95.30%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-base-mem.svg)
- [📄table](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-base.md)
- [📈time plot](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.126x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-default_base_vs_NOGIL.svg)

