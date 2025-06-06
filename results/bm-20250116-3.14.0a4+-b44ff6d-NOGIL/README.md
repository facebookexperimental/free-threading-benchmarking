# Results

- fork: python/b44ff6d0df9ec2d60be6
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [b44ff6d](https://github.com/python/cpython/commit/b44ff6d)
- commit date: 2025-01-16T15:57:04-08:00
- commit merge base: [27494dd9ad6032c29e273cd7f45c204c00d6512c](https://github.com/python/cpython/commit/27494dd9ad6032c29e273cd7f45c204c00d6512c)
- ref: b44ff6d0df9ec2d60be6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12820069445)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.94%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.12.6.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.126x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-base-mem.svg)
- [📄table](bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-base.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-base.svg)

