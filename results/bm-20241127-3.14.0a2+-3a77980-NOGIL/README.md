# Results

- fork: python/3a77980002845c22e5b2
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [3a77980](https://github.com/python/cpython/commit/3a77980)
- commit date: 2024-11-27T23:32:54+00:00
- commit merge base: [2247dd0f11058502f44b289df0e18ecc08be8657](https://github.com/python/cpython/commit/2247dd0f11058502f44b289df0e18ecc08be8657)
- ref: 3a77980002845c22e5b2

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12060274278)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980.json)

### vs. 3.12.6

- Geometric mean: 1.213x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.12.6.md)
- [📈time plot](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.244x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.13.0rc2.md)
- [📈time plot](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.258x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-base-mem.svg)
- [📄table](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-base.md)
- [📈time plot](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12060274278)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980.json)

### vs. 3.12.6

- Geometric mean: 1.266x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.12.6.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.291x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.13.0rc2.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.284x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [🧠memory plot](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-base-mem.svg)
- [📄table](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-base.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-base.svg)

