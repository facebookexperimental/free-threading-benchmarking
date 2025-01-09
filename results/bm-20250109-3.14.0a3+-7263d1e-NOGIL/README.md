# Results

- fork: Yhg1s/list_realloc
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [7263d1e](https://github.com/Yhg1s/cpython/commit/7263d1e)
- commit date: 2025-01-09T15:16:59+00:00
- commit merge base: [b725297cee9e5608b709f3c7291d974c97f68fff](https://github.com/python/cpython/commit/b725297cee9e5608b709f3c7291d974c97f68fff)
- ref: list_realloc

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12692934023)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e.json)

### vs. 3.12.6

- Geometric mean: 1.179x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e-vs-3.12.6.md)
- [📈time plot](bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.206x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e-vs-3.13.0rc2.svg)

