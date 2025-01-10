# Results

- fork: Yhg1s/list_realloc
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [89c4629](https://github.com/Yhg1s/cpython/commit/89c4629)
- commit date: 2025-01-09T17:14:03+01:00
- commit merge base: [b725297cee9e5608b709f3c7291d974c97f68fff](https://github.com/python/cpython/commit/b725297cee9e5608b709f3c7291d974c97f68fff)
- ref: list_realloc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12701330106)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-89c4629.json)

### vs. 3.12.6

- Geometric mean: 1.162x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-89c4629-vs-3.12.6.md)
- [📈time plot](bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-89c4629-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.189x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-89c4629-vs-3.13.0rc2.md)
- [📈time plot](bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-89c4629-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 91.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-89c4629-vs-base-mem.svg)
- [📄table](bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-89c4629-vs-base.md)
- [📈time plot](bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-89c4629-vs-base.svg)

