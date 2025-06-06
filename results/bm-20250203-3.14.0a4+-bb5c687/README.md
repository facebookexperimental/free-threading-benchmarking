# Results

- fork: python/bb5c6875d6e84bf2b4e1
- version: 3.14.0a4+
- config: 
- commit hash: [bb5c687](https://github.com/python/cpython/commit/bb5c687)
- commit date: 2025-02-03T16:42:12+00:00
- commit merge base: [75b628adebd4594529da25ea9915600f2872fc2b](https://github.com/python/cpython/commit/75b628adebd4594529da25ea9915600f2872fc2b)
- ref: bb5c6875d6e84bf2b4e1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13125607452)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.svg)

