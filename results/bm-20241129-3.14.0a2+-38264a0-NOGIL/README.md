# Results

- fork: python/38264a060a8178d58046
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [38264a0](https://github.com/python/cpython/commit/38264a0)
- commit date: 2024-11-29T21:03:39+00:00
- commit merge base: [15d6506d175780bb29e5fcde654e3860408aa93e](https://github.com/python/cpython/commit/15d6506d175780bb29e5fcde654e3860408aa93e)
- ref: 38264a060a8178d58046

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12091982894)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0.json)

### vs. 3.12.6

- Geometric mean: 1.261x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.286x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.276x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base-mem.svg)
- [📄table](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.275x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [📄table](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-default_base_vs_NOGIL.svg)

