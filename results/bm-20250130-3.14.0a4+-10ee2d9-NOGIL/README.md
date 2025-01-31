# Results

- fork: python/10ee2d9d3bcde27c75f1
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [10ee2d9](https://github.com/python/cpython/commit/10ee2d9)
- commit date: 2025-01-30T22:24:52+00:00
- commit merge base: [510fefdc625dd2ed2b6b3975314a59e291b94ae8](https://github.com/python/cpython/commit/510fefdc625dd2ed2b6b3975314a59e291b94ae8)
- ref: 10ee2d9d3bcde27c75f1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13063818762)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9.json)

### vs. 3.12.6

- Geometric mean: 1.051x slower (HPT: reliability of 99.93%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.md)
- [📈time plot](bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.127x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base-mem.svg)
- [📄table](bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base.md)
- [📈time plot](bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13063818762)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9.json)

### vs. 3.12.6

- Geometric mean: 1.050x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.md)
- [📈time plot](bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.134x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base-mem.svg)
- [📄table](bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base.md)
- [📈time plot](bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base.svg)

