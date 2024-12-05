# Results

- fork: python
- version: 3.14.0a2+
- config: 
- commit hash: [51cfa56](https://github.com/python/cpython/commit/51cfa56)
- commit date: 2024-12-04T10:30:51-08:00
- commit merge base: [6bc3e830a518112a4e242217807681e3908602f4](https://github.com/python/cpython/commit/6bc3e830a518112a4e242217807681e3908602f4)
- ref: 51cfa569e379f84b3418

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12173325879)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2%2B-51cfa56.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2%2B-51cfa56-vs-3.12.6.md)
- [📈time plot](bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2%2B-51cfa56-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x faster (HPT: reliability of 96.32%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2%2B-51cfa56-vs-3.13.0rc2.md)
- [📈time plot](bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2%2B-51cfa56-vs-3.13.0rc2.svg)

