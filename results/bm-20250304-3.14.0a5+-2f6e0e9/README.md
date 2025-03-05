# Results

- fork: python/2f6e0e9f7001769be746
- version: 3.14.0a5+
- config: 
- commit hash: [2f6e0e9](https://github.com/python/cpython/commit/2f6e0e9)
- commit date: 2025-03-04T18:04:04-05:00
- commit merge base: [cb67b44ca92f9930b3aa2aba8420c89d12a25303](https://github.com/python/cpython/commit/cb67b44ca92f9930b3aa2aba8420c89d12a25303)
- ref: 2f6e0e9f7001769be746

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13665665428)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250304-linux-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9.json)

### vs. 3.12.6

- Geometric mean: 1.114x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250304-linux-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9-vs-3.12.6.md)
- [📈time plot](bm-20250304-linux-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250304-linux-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250304-linux-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13665665428)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250304-vultr-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250304-vultr-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9-vs-3.12.6.md)
- [📈time plot](bm-20250304-vultr-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250304-vultr-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250304-vultr-x86_64-python-2f6e0e9f7001769be746-3.14.0a5%2B-2f6e0e9-vs-3.13.0rc2.svg)

