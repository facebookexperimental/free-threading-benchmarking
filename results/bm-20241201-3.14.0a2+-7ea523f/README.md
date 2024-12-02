# Results

- fork: python
- version: 3.14.0a2+
- config: 
- commit hash: [7ea523f](https://github.com/python/cpython/commit/7ea523f)
- commit date: 2024-12-01T19:29:27+00:00
- commit merge base: [04673d2f14414fce7a2372de3048190f66488e6e](https://github.com/python/cpython/commit/04673d2f14414fce7a2372de3048190f66488e6e)
- ref: 7ea523f47cdb4cf512a1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12110442594)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.md)
- [📈time plot](bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12110442594)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f.json)

### vs. 3.12.6

- Geometric mean: 1.033x faster (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.md)
- [📈time plot](bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x slower (HPT: reliability of 89.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.svg)

