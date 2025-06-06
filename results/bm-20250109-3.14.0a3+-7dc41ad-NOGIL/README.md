# Results

- fork: python/7dc41ad6a7826ffc675f
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [7dc41ad](https://github.com/python/cpython/commit/7dc41ad)
- commit date: 2025-01-09T21:26:00+05:30
- commit merge base: [b725297cee9e5608b709f3c7291d974c97f68fff](https://github.com/python/cpython/commit/b725297cee9e5608b709f3c7291d974c97f68fff)
- ref: 7dc41ad6a7826ffc675f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12748383082)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad.json)

### vs. 3.12.6

- Geometric mean: 1.165x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.12.6.md)
- [📈time plot](bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.192x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.13.0rc2.md)
- [📈time plot](bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 91.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-base-mem.svg)
- [📄table](bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-base.md)
- [📈time plot](bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-base.svg)

