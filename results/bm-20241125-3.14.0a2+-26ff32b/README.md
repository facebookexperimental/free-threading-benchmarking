# Results

- fork: python
- version: 3.14.0a2+
- config: 
- commit hash: [26ff32b](https://github.com/python/cpython/commit/26ff32b)
- commit date: 2024-11-25T15:34:01-06:00
- commit merge base: [5bb059fe606983814a445e4dcf9e96fd7cb4951a](https://github.com/python/cpython/commit/5bb059fe606983814a445e4dcf9e96fd7cb4951a)
- ref: 26ff32b30553e1f7b0cc

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12021293577)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.md)
- [📈time plot](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12021293577)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b.json)

### vs. 3.12.6

- Geometric mean: 1.037x faster (HPT: reliability of 99.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.md)
- [📈time plot](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x slower (HPT: reliability of 92.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.svg)

