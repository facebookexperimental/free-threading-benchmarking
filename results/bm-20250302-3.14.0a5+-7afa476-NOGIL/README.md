# Results

- fork: python/7afa476874b9a432ad6d
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [7afa476](https://github.com/python/cpython/commit/7afa476)
- commit date: 2025-03-02T13:21:34-08:00
- commit merge base: [c6513f7a627c8918a5e3f3733fa47d34a94ddff9](https://github.com/python/cpython/commit/c6513f7a627c8918a5e3f3733fa47d34a94ddff9)
- ref: 7afa476874b9a432ad6d

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13620845830)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250302-linux-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476.json)

### vs. 3.12.6

- Geometric mean: 1.003x slower (HPT: reliability of 98.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250302-linux-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-3.12.6.md)
- [📈time plot](bm-20250302-linux-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x slower (HPT: reliability of 99.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250302-linux-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-3.13.0rc2.md)
- [📈time plot](bm-20250302-linux-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250302-linux-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-base-mem.svg)
- [📄table](bm-20250302-linux-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-base.md)
- [📈time plot](bm-20250302-linux-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13620845830)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250302-vultr-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476.json)

### vs. 3.12.6

- Geometric mean: 1.049x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250302-vultr-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-3.12.6.md)
- [📈time plot](bm-20250302-vultr-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250302-vultr-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-3.13.0rc2.md)
- [📈time plot](bm-20250302-vultr-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.145x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250302-vultr-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-base-mem.svg)
- [📄table](bm-20250302-vultr-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-base.md)
- [📈time plot](bm-20250302-vultr-x86_64-python-7afa476874b9a432ad6d-3.14.0a5%2B-7afa476-vs-base.svg)

