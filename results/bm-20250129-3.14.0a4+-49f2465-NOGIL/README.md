# Results

- fork: python/49f24650e45414568724
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [49f2465](https://github.com/python/cpython/commit/49f2465)
- commit date: 2025-01-29T08:31:13-08:00
- commit merge base: [5ff2fbc026b14eadd41b8c14d83bb1eb832292dd](https://github.com/python/cpython/commit/5ff2fbc026b14eadd41b8c14d83bb1eb832292dd)
- ref: 49f24650e45414568724

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13164568577)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 99.95%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465-vs-3.12.6.md)
- [📈time plot](bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.96%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465-vs-3.13.0rc2.md)
- [📈time plot](bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465-vs-3.13.0rc2.svg)

