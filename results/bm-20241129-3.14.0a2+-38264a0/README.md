# Results

- fork: python/38264a060a8178d58046
- version: 3.14.0a2+
- config: 
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

- Geometric mean: 1.032x faster (HPT: reliability of 99.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 97.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 79.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base-mem.svg)
- [📄table](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base.svg)

