# Results

- fork: python/24c84d816f2f2ecb76b8
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [24c84d8](https://github.com/python/cpython/commit/24c84d8)
- commit date: 2025-01-22T12:48:33+00:00
- commit merge base: [a16ded10ad3952406280be5ab9ff86a476867b08](https://github.com/python/cpython/commit/a16ded10ad3952406280be5ab9ff86a476867b08)
- ref: 24c84d816f2f2ecb76b8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12917634273)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4%2B-24c84d8.json)

### vs. 3.12.6

- Geometric mean: 1.076x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4%2B-24c84d8-vs-3.12.6.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4%2B-24c84d8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4%2B-24c84d8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4%2B-24c84d8-vs-3.13.0rc2.svg)

