# Results

- fork: python/9ba281d871c4df3a3ac4
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [9ba281d](https://github.com/python/cpython/commit/9ba281d)
- commit date: 2025-01-31T15:27:08+00:00
- commit merge base: [60a85415aeb5a8be54b3c412d19a7444bf5ac757](https://github.com/python/cpython/commit/60a85415aeb5a8be54b3c412d19a7444bf5ac757)
- ref: 9ba281d871c4df3a3ac4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13090875764)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 99.62%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d-vs-3.12.6.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 99.94%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d-vs-3.13.0rc2.svg)

