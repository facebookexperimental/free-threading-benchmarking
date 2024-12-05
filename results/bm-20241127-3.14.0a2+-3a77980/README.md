# Results

- fork: python/3a77980002845c22e5b2
- version: 3.14.0a2+
- config: 
- commit hash: [3a77980](https://github.com/python/cpython/commit/3a77980)
- commit date: 2024-11-27T23:32:54+00:00
- commit merge base: [2247dd0f11058502f44b289df0e18ecc08be8657](https://github.com/python/cpython/commit/2247dd0f11058502f44b289df0e18ecc08be8657)
- ref: 3a77980002845c22e5b2

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12060274278)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.12.6.md)
- [📈time plot](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.13.0rc2.md)
- [📈time plot](bm-20241127-linux-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12060274278)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980.json)

### vs. 3.12.6

- Geometric mean: 1.037x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.12.6.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x slower (HPT: reliability of 73.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.13.0rc2.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-3a77980002845c22e5b2-3.14.0a2%2B-3a77980-vs-3.13.0rc2.svg)

