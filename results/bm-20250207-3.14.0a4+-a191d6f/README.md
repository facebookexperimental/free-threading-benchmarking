# Results

- fork: python/a191d6f78e10268845b2
- version: 3.14.0a4+
- config: 
- commit hash: [a191d6f](https://github.com/python/cpython/commit/a191d6f)
- commit date: 2025-02-07T00:37:05+01:00
- commit merge base: [b184abf074c0e1f379a238f07da5616460f36b93](https://github.com/python/cpython/commit/b184abf074c0e1f379a238f07da5616460f36b93)
- ref: a191d6f78e10268845b2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13190508540)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)
- [📈time plot](bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg)

