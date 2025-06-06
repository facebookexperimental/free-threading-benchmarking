# Results

- fork: python/8eebe4e6d02bb4ad3f1c
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [8eebe4e](https://github.com/python/cpython/commit/8eebe4e)
- commit date: 2025-01-02T14:02:54-05:00
- commit merge base: [c9356feef28e6dfc4dc32830d3427a5ae0e426e2](https://github.com/python/cpython/commit/c9356feef28e6dfc4dc32830d3427a5ae0e426e2)
- ref: 8eebe4e6d02bb4ad3f1c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12590039448)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e.json)

### vs. 3.12.6

- Geometric mean: 1.167x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.12.6.md)
- [📈time plot](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.194x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.234x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-base-mem.svg)
- [📄table](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-base.md)
- [📈time plot](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-base.svg)

