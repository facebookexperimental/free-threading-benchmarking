# Results

- fork: python/6bc3e830a518112a4e24
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [6bc3e83](https://github.com/python/cpython/commit/6bc3e83)
- commit date: 2024-12-04T14:30:38+01:00
- commit merge base: [bc0f2e945993747c8b1a6dd66cbe902fddd5758b](https://github.com/python/cpython/commit/bc0f2e945993747c8b1a6dd66cbe902fddd5758b)
- ref: 6bc3e830a518112a4e24

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12170581606)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2%2B-6bc3e83.json)

### vs. 3.12.6

- Geometric mean: 1.224x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2%2B-6bc3e83-vs-3.12.6.md)
- [📈time plot](bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2%2B-6bc3e83-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.249x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2%2B-6bc3e83-vs-3.13.0rc2.md)
- [📈time plot](bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2%2B-6bc3e83-vs-3.13.0rc2.svg)

