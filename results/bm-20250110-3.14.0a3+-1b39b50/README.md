# Results

- fork: python/1b39b502d33c68f52fd7
- version: 3.14.0a3+
- config: 
- commit hash: [1b39b50](https://github.com/python/cpython/commit/1b39b50)
- commit date: 2025-01-10T10:54:45-05:00
- commit merge base: [802556abfa008abe0bdd78e6f9e18bef71db90c1](https://github.com/python/cpython/commit/802556abfa008abe0bdd78e6f9e18bef71db90c1)
- ref: 1b39b502d33c68f52fd7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12719509421)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50-vs-3.12.6.md)
- [📈time plot](bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50-vs-3.13.0rc2.md)
- [📈time plot](bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50-vs-3.13.0rc2.svg)

