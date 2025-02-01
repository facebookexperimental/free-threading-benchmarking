# Results

- fork: python/31c82c28f927b7e55c7d
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [31c82c2](https://github.com/python/cpython/commit/31c82c2)
- commit date: 2025-01-31T11:17:37+00:00
- commit merge base: [674befbd7be3bffee66772ff9fdef168feda47ef](https://github.com/python/cpython/commit/674befbd7be3bffee66772ff9fdef168feda47ef)
- ref: 31c82c28f927b7e55c7d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13090866474)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2.json)

### vs. 3.12.6

- Geometric mean: 1.057x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.12.6.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.13.0rc2.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.13.0rc2.svg)

