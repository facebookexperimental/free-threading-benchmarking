# Results

- fork: python/e08b28235a863323ca3a
- version: 3.14.0a3+
- config: 
- commit hash: [e08b282](https://github.com/python/cpython/commit/e08b282)
- commit date: 2025-01-07T22:42:36+01:00
- commit merge base: [07e6aa2efc5b2c7ecbbdb41636013c64e335a2ba](https://github.com/python/cpython/commit/07e6aa2efc5b2c7ecbbdb41636013c64e335a2ba)
- ref: e08b28235a863323ca3a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12661624723)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.md)
- [📈time plot](bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.md)
- [📈time plot](bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.svg)

