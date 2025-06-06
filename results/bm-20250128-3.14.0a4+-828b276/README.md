# Results

- fork: python/828b27680f07f1ed8302
- version: 3.14.0a4+
- config: 
- commit hash: [828b276](https://github.com/python/cpython/commit/828b276)
- commit date: 2025-01-28T16:10:51-08:00
- commit merge base: [5c930a26fb78c40929f1b894efee1b07c6d828fd](https://github.com/python/cpython/commit/5c930a26fb78c40929f1b894efee1b07c6d828fd)
- ref: 828b27680f07f1ed8302

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13022081010)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-3.12.6.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-3.13.0rc2.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-3.13.0rc2.svg)

