# Results

- fork: python/bb5c6875d6e84bf2b4e1
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [bb5c687](https://github.com/python/cpython/commit/bb5c687)
- commit date: 2025-02-03T16:42:12+00:00
- commit merge base: [75b628adebd4594529da25ea9915600f2872fc2b](https://github.com/python/cpython/commit/75b628adebd4594529da25ea9915600f2872fc2b)
- ref: bb5c6875d6e84bf2b4e1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13125607452)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 99.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.md)
- [📈time plot](bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.md)
- [📈time plot](bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.125x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base-mem.svg)
- [📄table](bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base.md)
- [📈time plot](bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13125607452)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 99.96%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.130x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base-mem.svg)
- [📄table](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base.svg)

