# Results

- fork: python/main
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [d89a5f6](https://github.com/python/cpython/commit/d89a5f6)
- commit date: 2025-01-31T09:41:34-08:00
- commit merge base: [54f74b80aef8b581f2b124d150903cec83aff005](https://github.com/python/cpython/commit/54f74b80aef8b581f2b124d150903cec83aff005)
- ref: main

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13080498937)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 99.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-3.12.6.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 99.93%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.svg)

