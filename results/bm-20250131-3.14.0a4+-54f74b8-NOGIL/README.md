# Results

- fork: python/54f74b80aef8b581f2b1
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [54f74b8](https://github.com/python/cpython/commit/54f74b8)
- commit date: 2025-01-31T17:13:20+00:00
- commit merge base: [9ba281d871c4df3a3ac4cb7896d24ba0d42751a3](https://github.com/python/cpython/commit/9ba281d871c4df3a3ac4cb7896d24ba0d42751a3)
- ref: 54f74b80aef8b581f2b1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13090875764)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 99.62%, 1.01x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-3.12.6.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 99.94%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-3.13.0rc2.svg)

