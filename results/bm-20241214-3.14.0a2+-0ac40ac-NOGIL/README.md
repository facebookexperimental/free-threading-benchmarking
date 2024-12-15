# Results

- fork: python/0ac40acec045c4ce780c
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [0ac40ac](https://github.com/python/cpython/commit/0ac40ac)
- commit date: 2024-12-14T17:25:49+02:00
- commit merge base: [e2325c9db0650fc06d909eb2b5930c0573f24f71](https://github.com/python/cpython/commit/e2325c9db0650fc06d909eb2b5930c0573f24f71)
- ref: 0ac40acec045c4ce780c

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12334187396)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac.json)

### vs. 3.12.6

- Geometric mean: 1.156x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)
- [📈time plot](bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.185x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)
- [📈time plot](bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.246x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base-mem.svg)
- [📄table](bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.md)
- [📈time plot](bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12334187396)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac.json)

### vs. 3.12.6

- Geometric mean: 1.211x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)
- [📈time plot](bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.237x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)
- [📈time plot](bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.265x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base-mem.svg)
- [📄table](bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.md)
- [📈time plot](bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.svg)

