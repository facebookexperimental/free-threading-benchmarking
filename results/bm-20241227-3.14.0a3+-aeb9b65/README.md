# Results

- fork: python/aeb9b65aa26444529e4a
- version: 3.14.0a3+
- config: 
- commit hash: [aeb9b65](https://github.com/python/cpython/commit/aeb9b65)
- commit date: 2024-12-27T14:09:01-08:00
- commit merge base: [64173cd6f2d8dc95c6f8b67912d0edd1c1b707d5](https://github.com/python/cpython/commit/64173cd6f2d8dc95c6f8b67912d0edd1c1b707d5)
- ref: aeb9b65aa26444529e4a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12522108045)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.md)
- [📈time plot](bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.md)
- [📈time plot](bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.svg)

