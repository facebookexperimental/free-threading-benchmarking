# Results

- fork: python/b70a567575db37846bee
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [b70a567](https://github.com/python/cpython/commit/b70a567)
- commit date: 2025-01-13T17:58:11+01:00
- commit merge base: [53e8942e6938df3a32b783815f1bd4b76eed3dd0](https://github.com/python/cpython/commit/53e8942e6938df3a32b783815f1bd4b76eed3dd0)
- ref: b70a567575db37846bee

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12758478892)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567.json)

### vs. 3.12.6

- Geometric mean: 1.185x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)
- [📈time plot](bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.210x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.221x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base-mem.svg)
- [📄table](bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.md)
- [📈time plot](bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12758478892)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567.json)

### vs. 3.12.6

- Geometric mean: 1.161x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.188x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.231x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base-mem.svg)
- [📄table](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.svg)

