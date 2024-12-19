# Results

- fork: python/f802c8bf872ab882d305
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [f802c8b](https://github.com/python/cpython/commit/f802c8b)
- commit date: 2024-12-18T16:34:31+01:00
- commit merge base: [91c55085a959016250f1877e147ef379bb97dd12](https://github.com/python/cpython/commit/91c55085a959016250f1877e147ef379bb97dd12)
- ref: f802c8bf872ab882d305

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12403738651)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241218-linux-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b.json)

### vs. 3.12.6

- Geometric mean: 1.181x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241218-linux-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-3.12.6.md)
- [📈time plot](bm-20241218-linux-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.208x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241218-linux-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241218-linux-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.251x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20241218-linux-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-base-mem.svg)
- [📄table](bm-20241218-linux-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-base.md)
- [📈time plot](bm-20241218-linux-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12403738651)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241218-vultr-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b.json)

### vs. 3.12.6

- Geometric mean: 1.218x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241218-vultr-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-3.12.6.md)
- [📈time plot](bm-20241218-vultr-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.243x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241218-vultr-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241218-vultr-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.266x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241218-vultr-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-base-mem.svg)
- [📄table](bm-20241218-vultr-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-base.md)
- [📈time plot](bm-20241218-vultr-x86_64-python-f802c8bf872ab882d305-3.14.0a3%2B-f802c8b-vs-base.svg)

