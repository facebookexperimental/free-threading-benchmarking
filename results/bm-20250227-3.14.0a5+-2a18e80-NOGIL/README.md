# Results

- fork: python/2a18e80695ac1f05c95e
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [2a18e80](https://github.com/python/cpython/commit/2a18e80)
- commit date: 2025-02-27T09:36:41+00:00
- commit merge base: [fda056e64bdfcac3dd3d13eebda0a24994d83cb8](https://github.com/python/cpython/commit/fda056e64bdfcac3dd3d13eebda0a24994d83cb8)
- ref: 2a18e80695ac1f05c95e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13581932408)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-3.12.6.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-3.13.0rc2.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 54.50%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-base-mem.svg)
- [📄table](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-base.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.131x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-default_base_vs_NOGIL.svg)

