# Results

- fork: python/d05140f9f77d7dfc753d
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [d05140f](https://github.com/python/cpython/commit/d05140f)
- commit date: 2025-01-15T21:13:59+00:00
- commit merge base: [5eee2fe2b05c1a2836184e047fbd4176945cbf10](https://github.com/python/cpython/commit/5eee2fe2b05c1a2836184e047fbd4176945cbf10)
- ref: d05140f9f77d7dfc753d

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12799475571)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f.json)

### vs. 3.12.6

- Geometric mean: 1.073x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.md)
- [📈time plot](bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.129x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base-mem.svg)
- [📄table](bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base.md)
- [📈time plot](bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12797511462)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f.json)

### vs. 3.12.6

- Geometric mean: 1.053x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.127x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base-mem.svg)
- [📄table](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base.svg)

