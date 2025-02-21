# Results

- fork: python/d63af9540f6163104699
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [d63af95](https://github.com/python/cpython/commit/d63af95)
- commit date: 2025-02-20T23:58:58+00:00
- commit merge base: [6c450f44c283c61d0e1ada05ead9524a1fe97962](https://github.com/python/cpython/commit/6c450f44c283c61d0e1ada05ead9524a1fe97962)
- ref: d63af9540f6163104699

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13447306358)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250220-linux-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95.json)

### vs. 3.12.6

- Geometric mean: 1.007x slower (HPT: reliability of 99.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250220-linux-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-3.12.6.md)
- [📈time plot](bm-20250220-linux-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x slower (HPT: reliability of 99.79%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250220-linux-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-3.13.0rc2.md)
- [📈time plot](bm-20250220-linux-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250220-linux-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-base-mem.svg)
- [📄table](bm-20250220-linux-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-base.md)
- [📈time plot](bm-20250220-linux-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13447306358)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250220-vultr-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 99.96%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250220-vultr-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-3.12.6.md)
- [📈time plot](bm-20250220-vultr-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250220-vultr-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-3.13.0rc2.md)
- [📈time plot](bm-20250220-vultr-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.123x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250220-vultr-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-base-mem.svg)
- [📄table](bm-20250220-vultr-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-base.md)
- [📈time plot](bm-20250220-vultr-x86_64-python-d63af9540f6163104699-3.14.0a5%2B-d63af95-vs-base.svg)

