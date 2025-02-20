# Results

- fork: python/73801864d866c76ae26a
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [7380186](https://github.com/python/cpython/commit/7380186)
- commit date: 2025-02-19T19:16:38+00:00
- commit merge base: [ccf17323c218a2fdcf7f4845d3eaa74ebddefa44](https://github.com/python/cpython/commit/ccf17323c218a2fdcf7f4845d3eaa74ebddefa44)
- ref: 73801864d866c76ae26a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13425031100)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5%2B-7380186.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 99.97%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5%2B-7380186-vs-3.12.6.md)
- [📈time plot](bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5%2B-7380186-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5%2B-7380186-vs-3.13.0rc2.md)
- [📈time plot](bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5%2B-7380186-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5%2B-7380186-vs-base-mem.svg)
- [📄table](bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5%2B-7380186-vs-base.md)
- [📈time plot](bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5%2B-7380186-vs-base.svg)

