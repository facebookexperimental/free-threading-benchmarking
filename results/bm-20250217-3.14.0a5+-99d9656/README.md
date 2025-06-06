# Results

- fork: python/99d965635ae2ac4bffdc
- version: 3.14.0a5+
- config: 
- commit hash: [99d9656](https://github.com/python/cpython/commit/99d9656)
- commit date: 2025-02-17T20:06:08+00:00
- commit merge base: [6f07016bf01366da5939c4029c91b7f37ddddd55](https://github.com/python/cpython/commit/6f07016bf01366da5939c4029c91b7f37ddddd55)
- ref: 99d965635ae2ac4bffdc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13380695240)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.md)
- [📈time plot](bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.md)
- [📈time plot](bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.svg)

