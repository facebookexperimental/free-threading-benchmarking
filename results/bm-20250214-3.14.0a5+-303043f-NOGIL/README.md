# Results

- fork: python/303043f5062c1e7ffb79
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [303043f](https://github.com/python/cpython/commit/303043f)
- commit date: 2025-02-14T17:26:26+00:00
- commit merge base: [3402e133ef26736296c07992266a82b181a5d532](https://github.com/python/cpython/commit/3402e133ef26736296c07992266a82b181a5d532)
- ref: 303043f5062c1e7ffb79

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13336561391)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5%2B-303043f.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5%2B-303043f-vs-3.12.6.md)
- [📈time plot](bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5%2B-303043f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5%2B-303043f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5%2B-303043f-vs-3.13.0rc2.svg)

