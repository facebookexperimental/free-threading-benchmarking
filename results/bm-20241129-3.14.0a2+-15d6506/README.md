# Results

- fork: python
- version: 3.14.0a2+
- config: 
- commit hash: [15d6506](https://github.com/python/cpython/commit/15d6506)
- commit date: 2024-11-29T16:20:40+00:00
- commit merge base: [45c5cba318a19dda3ee6f9fc84781cc7a2fbde80](https://github.com/python/cpython/commit/45c5cba318a19dda3ee6f9fc84781cc7a2fbde80)
- ref: 15d6506d175780bb29e5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12129208802)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506.json)

### vs. 3.12.6

- Geometric mean: 1.031x faster (HPT: reliability of 99.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.12.6.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x slower (HPT: reliability of 97.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.13.0rc2.md)
- [📈time plot](bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.13.0rc2.svg)

