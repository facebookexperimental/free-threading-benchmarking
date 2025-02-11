# Results

- fork: python/1feaecc2bc42cb96f2d7
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [1feaecc](https://github.com/python/cpython/commit/1feaecc)
- commit date: 2025-02-10T23:46:36+02:00
- commit merge base: [516c70d4dd39e02bb365729a4b8aa93f9e6a3e82](https://github.com/python/cpython/commit/516c70d4dd39e02bb365729a4b8aa93f9e6a3e82)
- ref: 1feaecc2bc42cb96f2d7

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13253202595)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc.json)

### vs. 3.12.6

- Geometric mean: 1.034x slower (HPT: reliability of 99.61%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.md)
- [📈time plot](bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 99.95%, 1.02x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.127x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base-mem.svg)
- [📄table](bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base.md)
- [📈time plot](bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13253202595)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc.json)

### vs. 3.12.6

- Geometric mean: 1.050x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.md)
- [📈time plot](bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.136x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base-mem.svg)
- [📄table](bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base.md)
- [📈time plot](bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base.svg)

