# Results

- fork: python/39cd9728a6770d8fe793
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [39cd972](https://github.com/python/cpython/commit/39cd972)
- commit date: 2025-02-14T16:21:45-05:00
- commit merge base: [5a586c3e81ab53bb1f6c20a4c80b4eb69d429410](https://github.com/python/cpython/commit/5a586c3e81ab53bb1f6c20a4c80b4eb69d429410)
- ref: 39cd9728a6770d8fe793

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13338001011)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972.json)

### vs. 3.12.6

- Geometric mean: 1.048x slower (HPT: reliability of 99.97%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.md)
- [📈time plot](bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.md)
- [📈time plot](bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.126x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base-mem.svg)
- [📄table](bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base.md)
- [📈time plot](bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base.svg)

