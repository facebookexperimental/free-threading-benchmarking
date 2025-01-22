# Results

- fork: python/01bcf13a1c5bfca5124c
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [01bcf13](https://github.com/python/cpython/commit/01bcf13)
- commit date: 2025-01-21T23:28:32+00:00
- commit merge base: [29caec62ee0650493c83c778ee2ea50b0501bc41](https://github.com/python/cpython/commit/29caec62ee0650493c83c778ee2ea50b0501bc41)
- ref: 01bcf13a1c5bfca5124c

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12898483778)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13.json)

### vs. 3.12.6

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.12.6.md)
- [📈time plot](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.132x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.md)
- [📈time plot](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.128x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base-mem.svg)
- [📄table](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base.md)
- [📈time plot](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12898483778)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13.json)

### vs. 3.12.6

- Geometric mean: 1.075x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.12.6.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.155x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-default_base_vs_NOGIL.svg)

### vs. base

- [🧠memory plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base-mem.svg)
- [📄table](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base.svg)

