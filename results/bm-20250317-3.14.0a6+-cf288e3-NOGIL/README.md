# Results

- fork: python/cf288e3c250f5538aa63
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [cf288e3](https://github.com/python/cpython/commit/cf288e3)
- commit date: 2025-03-17T06:02:27+08:00
- commit merge base: [23cda583480fbc90cf19666a7514419ecad45b85](https://github.com/python/cpython/commit/23cda583480fbc90cf19666a7514419ecad45b85)
- ref: cf288e3c250f5538aa63

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13888945767)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base-mem.svg)
- [📄table](bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base.svg)

