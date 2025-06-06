# Results

- fork: python/9abbb58e3f023555473d
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [9abbb58](https://github.com/python/cpython/commit/9abbb58)
- commit date: 2025-01-24T22:31:52+00:00
- commit merge base: [3a3a6b86f4069a5a3561c65692937eb798053ae5](https://github.com/python/cpython/commit/3a3a6b86f4069a5a3561c65692937eb798053ae5)
- ref: 9abbb58e3f023555473d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12959859834)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58.json)

### vs. 3.12.6

- Geometric mean: 1.063x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.55x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.md)
- [📈time plot](bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.094x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.54x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.md)
- [📈time plot](bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.140x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base-mem.svg)
- [📄table](bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base.md)
- [📈time plot](bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base.svg)

