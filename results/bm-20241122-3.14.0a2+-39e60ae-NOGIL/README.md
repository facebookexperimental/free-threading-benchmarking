# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [39e60ae](https://github.com/python/cpython/commit/39e60ae)
- commit date: 2024-11-22T16:02:51-08:00
- commit merge base: [d24a22e9b6377797c3b602945347096fbe065670](https://github.com/python/cpython/commit/d24a22e9b6377797c3b602945347096fbe065670)
- ref: 39e60aeb3837f1f23d8b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11982244918)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.md)
- [📈time plot](bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base-mem.svg)
- [📄table](bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.md)
- [📈time plot](bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11982244918)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 66.59%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base-mem.svg)
- [📄table](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-default_base_vs_NOGIL.svg)

