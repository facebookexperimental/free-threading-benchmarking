# Results

- fork: python/d4544cb232dee5f836a6
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [d4544cb](https://github.com/python/cpython/commit/d4544cb)
- commit date: 2025-01-17T23:43:17+01:00
- commit merge base: [13c4def692228f09df0b30c5f93bc515e89fc77f](https://github.com/python/cpython/commit/13c4def692228f09df0b30c5f93bc515e89fc77f)
- ref: d4544cb232dee5f836a6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12838958316)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250117-vultr-x86_64-python-d4544cb232dee5f836a6-3.14.0a4%2B-d4544cb.json)

### vs. 3.12.6

- Geometric mean: 1.060x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250117-vultr-x86_64-python-d4544cb232dee5f836a6-3.14.0a4%2B-d4544cb-vs-3.12.6.md)
- [📈time plot](bm-20250117-vultr-x86_64-python-d4544cb232dee5f836a6-3.14.0a4%2B-d4544cb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250117-vultr-x86_64-python-d4544cb232dee5f836a6-3.14.0a4%2B-d4544cb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250117-vultr-x86_64-python-d4544cb232dee5f836a6-3.14.0a4%2B-d4544cb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.135x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250117-vultr-x86_64-python-d4544cb232dee5f836a6-3.14.0a4%2B-d4544cb-vs-base-mem.svg)
- [📄table](bm-20250117-vultr-x86_64-python-d4544cb232dee5f836a6-3.14.0a4%2B-d4544cb-vs-base.md)
- [📈time plot](bm-20250117-vultr-x86_64-python-d4544cb232dee5f836a6-3.14.0a4%2B-d4544cb-vs-base.svg)

