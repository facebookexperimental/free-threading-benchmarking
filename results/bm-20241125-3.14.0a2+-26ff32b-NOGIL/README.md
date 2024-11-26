# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
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

- Geometric mean: 1.196x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.md)
- [📈time plot](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.226x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.248x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-base-mem.svg)
- [📄table](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-base.md)
- [📈time plot](bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12021293577)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b.json)

### vs. 3.12.6

- Geometric mean: 1.259x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.md)
- [📈time plot](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.284x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.277x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [🧠memory plot](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-base-mem.svg)
- [📄table](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-base.md)
- [📈time plot](bm-20241125-vultr-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-base.svg)

