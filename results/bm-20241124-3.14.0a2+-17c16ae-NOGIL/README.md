# Results

- fork: python/17c16aea66b606d66f71
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [17c16ae](https://github.com/python/cpython/commit/17c16ae)
- commit date: 2024-11-24T14:42:50-08:00
- commit merge base: [307c63358681d669ae39e5ecd814bded4a93443a](https://github.com/python/cpython/commit/307c63358681d669ae39e5ecd814bded4a93443a)
- ref: 17c16aea66b606d66f71

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12000941135)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.md)
- [📈time plot](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [🧠memory plot](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base-mem.svg)
- [📄table](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base.md)
- [📈time plot](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base.svg)

