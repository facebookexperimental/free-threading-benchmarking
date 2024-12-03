# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [15d6506](https://github.com/python/cpython/commit/15d6506)
- commit date: 2024-11-29T16:20:40+00:00
- commit merge base: [45c5cba318a19dda3ee6f9fc84781cc7a2fbde80](https://github.com/python/cpython/commit/45c5cba318a19dda3ee6f9fc84781cc7a2fbde80)
- ref: 15d6506d175780bb29e5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12129922359)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506.json)

### vs. 3.12.6

- Geometric mean: 1.259x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.12.6.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.284x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.13.0rc2.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.273x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [🧠memory plot](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-base-mem.svg)
- [📄table](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-base.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-base.svg)

