# Results

- fork: python/3829104ab412a47bf3f3
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [3829104](https://github.com/python/cpython/commit/3829104)
- commit date: 2025-01-17T16:49:16-08:00
- commit merge base: [8174770d311ba09c07a47cc3ae90a1db2e7d7708](https://github.com/python/cpython/commit/8174770d311ba09c07a47cc3ae90a1db2e7d7708)
- ref: 3829104ab412a47bf3f3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12919728922)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4%2B-3829104.json)

### vs. 3.12.6

- Geometric mean: 1.060x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4%2B-3829104-vs-3.12.6.md)
- [📈time plot](bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4%2B-3829104-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.090x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4%2B-3829104-vs-3.13.0rc2.md)
- [📈time plot](bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4%2B-3829104-vs-3.13.0rc2.svg)

