# Results

- fork: python/736ad664e0c3be05fad7
- version: 3.14.0a5+
- config: 
- commit hash: [736ad66](https://github.com/python/cpython/commit/736ad66)
- commit date: 2025-02-18T23:45:02+00:00
- commit merge base: [857bdba0ac66ed7963e9fca45ab1a5f7a32b4bfb](https://github.com/python/cpython/commit/857bdba0ac66ed7963e9fca45ab1a5f7a32b4bfb)
- ref: 736ad664e0c3be05fad7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13402753944)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250218-vultr-x86_64-python-736ad664e0c3be05fad7-3.14.0a5%2B-736ad66.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250218-vultr-x86_64-python-736ad664e0c3be05fad7-3.14.0a5%2B-736ad66-vs-3.12.6.md)
- [📈time plot](bm-20250218-vultr-x86_64-python-736ad664e0c3be05fad7-3.14.0a5%2B-736ad66-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 99.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250218-vultr-x86_64-python-736ad664e0c3be05fad7-3.14.0a5%2B-736ad66-vs-3.13.0rc2.md)
- [📈time plot](bm-20250218-vultr-x86_64-python-736ad664e0c3be05fad7-3.14.0a5%2B-736ad66-vs-3.13.0rc2.svg)

