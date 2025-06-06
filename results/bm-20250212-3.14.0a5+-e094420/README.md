# Results

- fork: python/e09442089eb86d88d4b5
- version: 3.14.0a5+
- config: 
- commit hash: [e094420](https://github.com/python/cpython/commit/e094420)
- commit date: 2025-02-12T18:09:15-05:00
- commit merge base: [791cdfe1416a591e240b8ffc6f10eb6f659c8277](https://github.com/python/cpython/commit/791cdfe1416a591e240b8ffc6f10eb6f659c8277)
- ref: e09442089eb86d88d4b5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13297620377)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.12.6.md)
- [📈time plot](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.13.0rc2.md)
- [📈time plot](bm-20250212-vultr-x86_64-python-e09442089eb86d88d4b5-3.14.0a5%2B-e094420-vs-3.13.0rc2.svg)

