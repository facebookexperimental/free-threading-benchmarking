# Results

- fork: python/dbd23790dbd662169905
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [dbd2379](https://github.com/python/cpython/commit/dbd2379)
- commit date: 2024-11-23T16:41:01-05:00
- commit merge base: [e3038e976b25a58f512d8c7083a752c89436eb0d](https://github.com/python/cpython/commit/e3038e976b25a58f512d8c7083a752c89436eb0d)
- ref: dbd23790dbd662169905

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11991495406)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.md)
- [📈time plot](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.md)
- [📈time plot](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [🧠memory plot](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base-mem.svg)
- [📄table](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base.md)
- [📈time plot](bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base.svg)

