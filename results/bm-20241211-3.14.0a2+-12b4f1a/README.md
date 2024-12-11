# Results

- fork: python/12b4f1a5a175d4dcec27
- version: 3.14.0a2+
- config: 
- commit hash: [12b4f1a](https://github.com/python/cpython/commit/12b4f1a)
- commit date: 2024-12-11T00:09:55+00:00
- commit merge base: [51216857ca8283f5b41c8cf9874238da56da4968](https://github.com/python/cpython/commit/51216857ca8283f5b41c8cf9874238da56da4968)
- ref: 12b4f1a5a175d4dcec27

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12267183018)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241211-linux-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a.json)

### vs. 3.12.6

- Geometric mean: 1.113x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241211-linux-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a-vs-3.12.6.md)
- [📈time plot](bm-20241211-linux-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241211-linux-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241211-linux-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12267183018)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241211-vultr-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a.json)

### vs. 3.12.6

- Geometric mean: 1.081x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241211-vultr-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a-vs-3.12.6.md)
- [📈time plot](bm-20241211-vultr-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241211-vultr-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241211-vultr-x86_64-python-12b4f1a5a175d4dcec27-3.14.0a2%2B-12b4f1a-vs-3.13.0rc2.svg)

