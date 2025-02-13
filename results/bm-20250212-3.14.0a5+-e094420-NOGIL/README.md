# Results

- fork: python/e09442089eb86d88d4b5
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [e094420](https://github.com/python/cpython/commit/e094420)
- commit date: 2025-02-12T18:09:15-05:00
- commit merge base: [791cdfe1416a591e240b8ffc6f10eb6f659c8277](https://github.com/python/cpython/commit/791cdfe1416a591e240b8ffc6f10eb6f659c8277)
- ref: e09442089eb86d88d4b5

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13297620377)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250212-linux-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 99.84%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250212-linux-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.12.6.md)
- [📈time plot](bm-20250212-linux-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 99.96%, 1.02x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250212-linux-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.13.0rc2.md)
- [📈time plot](bm-20250212-linux-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.116x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250212-linux-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-base-mem.svg)
- [📄table](bm-20250212-linux-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-base.md)
- [📈time plot](bm-20250212-linux-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13297620377)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420.json)

### vs. 3.12.6

- Geometric mean: 1.055x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.12.6.md)
- [📈time plot](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.13.0rc2.md)
- [📈time plot](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.131x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-base-mem.svg)
- [📄table](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-base.md)
- [📈time plot](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-base.svg)

