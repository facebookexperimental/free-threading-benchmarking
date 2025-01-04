# Results

- fork: python/f1574859d7d6cd259f86
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [f157485](https://github.com/python/cpython/commit/f157485)
- commit date: 2025-01-03T21:48:47+00:00
- commit merge base: [b75ed951d4de8ba85349d80c8e7f097b3cd6052f](https://github.com/python/cpython/commit/b75ed951d4de8ba85349d80c8e7f097b3cd6052f)
- ref: f1574859d7d6cd259f86

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12605737751)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250103-linux-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485.json)

### vs. 3.12.6

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250103-linux-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-3.12.6.md)
- [📈time plot](bm-20250103-linux-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.129x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250103-linux-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-3.13.0rc2.md)
- [📈time plot](bm-20250103-linux-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.166x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250103-linux-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-base-mem.svg)
- [📄table](bm-20250103-linux-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-base.md)
- [📈time plot](bm-20250103-linux-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12604534528)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485.json)

### vs. 3.12.6

- Geometric mean: 1.168x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-3.12.6.md)
- [📈time plot](bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.195x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-3.13.0rc2.md)
- [📈time plot](bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.231x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-base-mem.svg)
- [📄table](bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-base.md)
- [📈time plot](bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3%2B-f157485-vs-base.svg)

