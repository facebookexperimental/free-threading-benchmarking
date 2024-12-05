# Results

- fork: python/328187cc4fcdd578db42
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [328187c](https://github.com/python/cpython/commit/328187c)
- commit date: 2024-11-30T18:39:39+00:00
- commit merge base: [4e0a4cafe8d8ecb43db62aed1d5671af583104e7](https://github.com/python/cpython/commit/4e0a4cafe8d8ecb43db62aed1d5671af583104e7)
- ref: 328187cc4fcdd578db42

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12100542415)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c.json)

### vs. 3.12.6

- Geometric mean: 1.209x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.md)
- [📈time plot](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.239x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.251x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base-mem.svg)
- [📄table](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base.md)
- [📈time plot](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12100542415)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c.json)

### vs. 3.12.6

- Geometric mean: 1.254x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.md)
- [📈time plot](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.279x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.270x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [🧠memory plot](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base-mem.svg)
- [📄table](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base.md)
- [📈time plot](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base.svg)

