# Results

- fork: python/f97e4098ff71a6488fd3
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [f97e409](https://github.com/python/cpython/commit/f97e409)
- commit date: 2025-03-02T18:01:45-08:00
- commit merge base: [7afa476874b9a432ad6dbe9fb3e65d62f2999f88](https://github.com/python/cpython/commit/7afa476874b9a432ad6dbe9fb3e65d62f2999f88)
- ref: f97e4098ff71a6488fd3

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13624667507)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409.json)

### vs. 3.12.6

- Geometric mean: 1.001x slower (HPT: reliability of 99.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-3.12.6.md)
- [📈time plot](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x slower (HPT: reliability of 99.68%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-3.13.0rc2.md)
- [📈time plot](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 63.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-base-mem.svg)
- [📄table](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-base.md)
- [📈time plot](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.118x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [📄table](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250302-linux-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-default_base_vs_NOGIL.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13624667507)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-3.12.6.md)
- [📈time plot](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-3.13.0rc2.md)
- [📈time plot](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-base-mem.svg)
- [📄table](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-base.md)
- [📈time plot](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.141x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250302-vultr-x86_64-python-f97e4098ff71a6488fd3-3.14.0a5%2B-f97e409-vs-default_base_vs_NOGIL.svg)

