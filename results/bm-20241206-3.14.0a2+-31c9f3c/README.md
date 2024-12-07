# Results

- fork: python/31c9f3ced293492b38e7
- version: 3.14.0a2+
- config: 
- commit hash: [31c9f3c](https://github.com/python/cpython/commit/31c9f3c)
- commit date: 2024-12-06T21:39:45+00:00
- commit merge base: [0fc4063747c96223575f6f5a0562eddf2ed0ed62](https://github.com/python/cpython/commit/0fc4063747c96223575f6f5a0562eddf2ed0ed62)
- ref: 31c9f3ced293492b38e7

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12208181088)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241206-linux-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c.json)

### vs. 3.12.6

- Geometric mean: 1.119x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241206-linux-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c-vs-3.12.6.md)
- [📈time plot](bm-20241206-linux-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241206-linux-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241206-linux-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12208181088)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241206-vultr-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c.json)

### vs. 3.12.6

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241206-vultr-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c-vs-3.12.6.md)
- [📈time plot](bm-20241206-vultr-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 93.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241206-vultr-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241206-vultr-x86_64-python-31c9f3ced293492b38e7-3.14.0a2%2B-31c9f3c-vs-3.13.0rc2.svg)

