# Results

- fork: python/55815a6474c59001f023
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [55815a6](https://github.com/python/cpython/commit/55815a6)
- commit date: 2025-03-14T21:23:27+00:00
- commit merge base: [26511993e63265ea5928aabe6af96d89e20f0553](https://github.com/python/cpython/commit/26511993e63265ea5928aabe6af96d89e20f0553)
- ref: 55815a6474c59001f023

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13867522983)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)
- [📈time plot](bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base-mem.svg)
- [📄table](bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.md)
- [📈time plot](bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.svg)

