# Results

- fork: python/ab11c097052757b79060
- version: 3.14.0a5+
- config: 
- commit hash: [ab11c09](https://github.com/python/cpython/commit/ab11c09)
- commit date: 2025-02-28T16:05:36+00:00
- commit merge base: [003e6d2b9776c07147a9c628eb028fd2ac3f0008](https://github.com/python/cpython/commit/003e6d2b9776c07147a9c628eb028fd2ac3f0008)
- ref: ab11c097052757b79060

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13594439311)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5%2B-ab11c09.json)

### vs. 3.12.6

- Geometric mean: 1.111x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5%2B-ab11c09-vs-3.12.6.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5%2B-ab11c09-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5%2B-ab11c09-vs-3.13.0rc2.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5%2B-ab11c09-vs-3.13.0rc2.svg)

