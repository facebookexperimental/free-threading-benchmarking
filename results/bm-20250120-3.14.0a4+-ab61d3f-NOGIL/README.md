# Results

- fork: python/ab61d3f4303d14a413bc
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [ab61d3f](https://github.com/python/cpython/commit/ab61d3f)
- commit date: 2025-01-20T17:09:23+00:00
- commit merge base: [0a6412f9cc9e694e76299cfbd73ec969b7d47af6](https://github.com/python/cpython/commit/0a6412f9cc9e694e76299cfbd73ec969b7d47af6)
- ref: ab61d3f4303d14a413bc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12894574940)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250120-vultr-x86_64-python-ab61d3f4303d14a413bc-3.14.0a4%2B-ab61d3f.json)

### vs. 3.12.6

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-ab61d3f4303d14a413bc-3.14.0a4%2B-ab61d3f-vs-3.12.6.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-ab61d3f4303d14a413bc-3.14.0a4%2B-ab61d3f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.112x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-ab61d3f4303d14a413bc-3.14.0a4%2B-ab61d3f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-ab61d3f4303d14a413bc-3.14.0a4%2B-ab61d3f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.031x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250120-vultr-x86_64-python-ab61d3f4303d14a413bc-3.14.0a4%2B-ab61d3f-vs-base-mem.svg)
- [📄table](bm-20250120-vultr-x86_64-python-ab61d3f4303d14a413bc-3.14.0a4%2B-ab61d3f-vs-base.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-ab61d3f4303d14a413bc-3.14.0a4%2B-ab61d3f-vs-base.svg)

