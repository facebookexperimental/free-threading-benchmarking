# Results

- fork: python/39e69a7cd54d44c9061d
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [39e69a7](https://github.com/python/cpython/commit/39e69a7)
- commit date: 2024-12-19T15:38:42-08:00
- commit merge base: [c14db202750ff9eaf3919298f1172270b7dfd64e](https://github.com/python/cpython/commit/c14db202750ff9eaf3919298f1172270b7dfd64e)
- ref: 39e69a7cd54d44c9061d

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12423087893)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241219-linux-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7.json)

### vs. 3.12.6

- Geometric mean: 1.143x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241219-linux-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-3.12.6.md)
- [📈time plot](bm-20241219-linux-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.172x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241219-linux-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-3.13.0rc2.md)
- [📈time plot](bm-20241219-linux-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.216x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20241219-linux-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-base-mem.svg)
- [📄table](bm-20241219-linux-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-base.md)
- [📈time plot](bm-20241219-linux-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12423087893)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7.json)

### vs. 3.12.6

- Geometric mean: 1.189x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-3.12.6.md)
- [📈time plot](bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.215x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-3.13.0rc2.md)
- [📈time plot](bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.246x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-base-mem.svg)
- [📄table](bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-base.md)
- [📈time plot](bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3%2B-39e69a7-vs-base.svg)

