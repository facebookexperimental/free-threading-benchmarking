# Results

- fork: python/b5454509612870dd0e09
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [b545450](https://github.com/python/cpython/commit/b545450)
- commit date: 2025-02-28T19:29:20+00:00
- commit merge base: [fdcbc29f26448f47201ec40fcf3b6405631c85d3](https://github.com/python/cpython/commit/fdcbc29f26448f47201ec40fcf3b6405631c85d3)
- ref: b5454509612870dd0e09

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13595977471)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250228-vultr-x86_64-python-b5454509612870dd0e09-3.14.0a5%2B-b545450.json)

### vs. 3.12.6

- Geometric mean: 1.050x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250228-vultr-x86_64-python-b5454509612870dd0e09-3.14.0a5%2B-b545450-vs-3.12.6.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-b5454509612870dd0e09-3.14.0a5%2B-b545450-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250228-vultr-x86_64-python-b5454509612870dd0e09-3.14.0a5%2B-b545450-vs-3.13.0rc2.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-b5454509612870dd0e09-3.14.0a5%2B-b545450-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.137x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250228-vultr-x86_64-python-b5454509612870dd0e09-3.14.0a5%2B-b545450-vs-base-mem.svg)
- [📄table](bm-20250228-vultr-x86_64-python-b5454509612870dd0e09-3.14.0a5%2B-b545450-vs-base.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-b5454509612870dd0e09-3.14.0a5%2B-b545450-vs-base.svg)

