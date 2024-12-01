# Results

- fork: python
- version: 3.14.0a2+
- config: 
- commit hash: [328187c](https://github.com/python/cpython/commit/328187c)
- commit date: 2024-11-30T18:39:39+00:00
- commit merge base: [4e0a4cafe8d8ecb43db62aed1d5671af583104e7](https://github.com/python/cpython/commit/4e0a4cafe8d8ecb43db62aed1d5671af583104e7)
- ref: 328187cc4fcdd578db42

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12100542415)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.md)
- [📈time plot](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12100542415)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c.json)

### vs. 3.12.6

- Geometric mean: 1.033x faster (HPT: reliability of 98.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.md)
- [📈time plot](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 98.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.svg)

