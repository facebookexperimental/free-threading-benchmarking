# Results

- fork: python/2f1cee8477e22bfc36a7
- version: 3.14.0a2+
- config: 
- commit hash: [2f1cee8](https://github.com/python/cpython/commit/2f1cee8)
- commit date: 2024-12-05T08:25:06+08:00
- commit merge base: [94b8f8b40943bf38cf5c454773a3fb8f4ff71e01](https://github.com/python/cpython/commit/94b8f8b40943bf38cf5c454773a3fb8f4ff71e01)
- ref: 2f1cee8477e22bfc36a7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12170805753)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241205-vultr-x86_64-python-2f1cee8477e22bfc36a7-3.14.0a2%2B-2f1cee8.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241205-vultr-x86_64-python-2f1cee8477e22bfc36a7-3.14.0a2%2B-2f1cee8-vs-3.12.6.md)
- [📈time plot](bm-20241205-vultr-x86_64-python-2f1cee8477e22bfc36a7-3.14.0a2%2B-2f1cee8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 98.41%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241205-vultr-x86_64-python-2f1cee8477e22bfc36a7-3.14.0a2%2B-2f1cee8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241205-vultr-x86_64-python-2f1cee8477e22bfc36a7-3.14.0a2%2B-2f1cee8-vs-3.13.0rc2.svg)

