# Results

- fork: python/c3ae5c9e4ad121f8ba60
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [c3ae5c9](https://github.com/python/cpython/commit/c3ae5c9)
- commit date: 2025-01-31T12:12:24+00:00
- commit merge base: [31c82c28f927b7e55c7dfdd548322c6c36760278](https://github.com/python/cpython/commit/31c82c28f927b7e55c7dfdd548322c6c36760278)
- ref: c3ae5c9e4ad121f8ba60

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13090866474)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 99.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.12.6.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 99.94%, 1.02x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.029x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base-mem.svg)
- [📄table](bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base.md)
- [📈time plot](bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base.svg)

