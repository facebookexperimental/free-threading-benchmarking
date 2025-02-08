# Results

- fork: python/a1417b211f0bb9582b00
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [a1417b2](https://github.com/python/cpython/commit/a1417b2)
- commit date: 2025-02-07T22:39:54+00:00
- commit merge base: [2248a9c153092b920ff68b0eee009c04dbe19f61](https://github.com/python/cpython/commit/2248a9c153092b920ff68b0eee009c04dbe19f61)
- ref: a1417b211f0bb9582b00

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13210286437)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2.json)

### vs. 3.12.6

- Geometric mean: 1.004x faster (HPT: reliability of 94.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.md)
- [📈time plot](bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x slower (HPT: reliability of 99.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.md)
- [📈time plot](bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base-mem.svg)
- [📄table](bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base.md)
- [📈time plot](bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13210286437)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2.json)

### vs. 3.12.6

- Geometric mean: 1.049x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.md)
- [📈time plot](bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.md)
- [📈time plot](bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.138x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base-mem.svg)
- [📄table](bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base.md)
- [📈time plot](bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base.svg)

