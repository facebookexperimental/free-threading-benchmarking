# Results

- fork: python/3b231be8f000ae59faa0
- version: 3.14.0a3+
- config: 
- commit hash: [3b231be](https://github.com/python/cpython/commit/3b231be)
- commit date: 2025-01-05T22:58:31+01:00
- commit merge base: [2228e92da31ca7344a163498f848973a1b356597](https://github.com/python/cpython/commit/2228e92da31ca7344a163498f848973a1b356597)
- ref: 3b231be8f000ae59faa0

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12624266444)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be.json)

### vs. 3.12.6

- Geometric mean: 1.125x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.md)
- [📈time plot](bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.md)
- [📈time plot](bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12624266444)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.md)
- [📈time plot](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.md)
- [📈time plot](bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.svg)

