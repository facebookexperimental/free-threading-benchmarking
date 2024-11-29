# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [b83be9c](https://github.com/python/cpython/commit/b83be9c)
- commit date: 2024-11-28T19:03:09+02:00
- commit merge base: [20657fbdb14d50ca4ec115da0cbef155871d8d33](https://github.com/python/cpython/commit/20657fbdb14d50ca4ec115da0cbef155871d8d33)
- ref: b83be9c9718aac42d0d8

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12076969482)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c.json)

### vs. 3.12.6

- Geometric mean: 1.206x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.12.6.md)
- [📈time plot](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.236x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.244x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-base-mem.svg)
- [📄table](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-base.md)
- [📈time plot](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12076969482)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c.json)

### vs. 3.12.6

- Geometric mean: 1.258x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.12.6.md)
- [📈time plot](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.283x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.278x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [🧠memory plot](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-base-mem.svg)
- [📄table](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-base.md)
- [📈time plot](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-base.svg)

