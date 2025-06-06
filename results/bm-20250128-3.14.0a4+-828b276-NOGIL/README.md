# Results

- fork: python/828b27680f07f1ed8302
- version: 3.14.0a4+
- config: NOGIL
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

- Geometric mean: 1.076x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-3.12.6.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-3.13.0rc2.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.155x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-base-mem.svg)
- [📄table](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-base.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-828b27680f07f1ed8302-3.14.0a4%2B-828b276-vs-base.svg)

