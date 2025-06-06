# Results

- fork: python/dbd23790dbd662169905
- version: 3.14.0a2+
- config: 
- commit hash: [dbd2379](https://github.com/python/cpython/commit/dbd2379)
- commit date: 2024-11-23T16:41:01-05:00
- commit merge base: [e3038e976b25a58f512d8c7083a752c89436eb0d](https://github.com/python/cpython/commit/e3038e976b25a58f512d8c7083a752c89436eb0d)
- ref: dbd23790dbd662169905

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11991495406)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-pystats.json)
- [pystats table](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-pystats.md)
- [raw results](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.27%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.md)
- [📈time plot](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 98.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.md)
- [📈time plot](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.svg)

