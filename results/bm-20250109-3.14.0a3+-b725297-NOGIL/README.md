# Results

- fork: python/b725297cee9e5608b709
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [b725297](https://github.com/python/cpython/commit/b725297)
- commit date: 2025-01-09T18:15:13+03:00
- commit merge base: [43ac9f505903ba806aa6a5d93e6a67beb04bebc4](https://github.com/python/cpython/commit/43ac9f505903ba806aa6a5d93e6a67beb04bebc4)
- ref: b725297cee9e5608b709

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12701330106)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3%2B-b725297.json)

### vs. 3.12.6

- Geometric mean: 1.165x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3%2B-b725297-vs-3.12.6.md)
- [📈time plot](bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3%2B-b725297-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.192x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3%2B-b725297-vs-3.13.0rc2.md)
- [📈time plot](bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3%2B-b725297-vs-3.13.0rc2.svg)

