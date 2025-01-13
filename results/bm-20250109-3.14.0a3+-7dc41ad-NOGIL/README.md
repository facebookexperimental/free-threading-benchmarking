# Results

- fork: python/7dc41ad6a7826ffc675f
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [7dc41ad](https://github.com/python/cpython/commit/7dc41ad)
- commit date: 2025-01-09T21:26:00+05:30
- commit merge base: [b725297cee9e5608b709f3c7291d974c97f68fff](https://github.com/python/cpython/commit/b725297cee9e5608b709f3c7291d974c97f68fff)
- ref: 7dc41ad6a7826ffc675f

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12738766432)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad.json)

### vs. 3.12.6

- Geometric mean: 1.151x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.12.6.md)
- [📈time plot](bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.181x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.13.0rc2.md)
- [📈time plot](bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.13.0rc2.svg)

