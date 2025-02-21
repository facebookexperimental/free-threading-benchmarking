# Results

- fork: python/6c450f44c283c61d0e1a
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [6c450f4](https://github.com/python/cpython/commit/6c450f4)
- commit date: 2025-02-20T13:32:57-08:00
- commit merge base: [69426fcee7fcecbe34be66d2c5b58b6d0ffe2809](https://github.com/python/cpython/commit/69426fcee7fcecbe34be66d2c5b58b6d0ffe2809)
- ref: 6c450f44c283c61d0e1a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13465084758)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5%2B-6c450f4.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 99.97%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5%2B-6c450f4-vs-3.12.6.md)
- [📈time plot](bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5%2B-6c450f4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 99.98%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5%2B-6c450f4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5%2B-6c450f4-vs-3.13.0rc2.svg)

