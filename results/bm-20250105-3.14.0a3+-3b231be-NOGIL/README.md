# Results

- fork: python/3b231be8f000ae59faa0
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [3b231be](https://github.com/python/cpython/commit/3b231be)
- commit date: 2025-01-05T22:58:31+01:00
- commit merge base: [2228e92da31ca7344a163498f848973a1b356597](https://github.com/python/cpython/commit/2228e92da31ca7344a163498f848973a1b356597)
- ref: 3b231be8f000ae59faa0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12624266444)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be.json)

### vs. 3.12.6

- Geometric mean: 1.173x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.md)
- [📈time plot](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.199x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.md)
- [📈time plot](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.243x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base-mem.svg)
- [📄table](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base.md)
- [📈time plot](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base.svg)

