# Results

- fork: python/86c1a60d5a28cfb51f88
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [86c1a60](https://github.com/python/cpython/commit/86c1a60)
- commit date: 2025-01-22T09:22:25+08:00
- commit merge base: [767cf708449fbf13826d379ecef64af97d779510](https://github.com/python/cpython/commit/767cf708449fbf13826d379ecef64af97d779510)
- ref: 86c1a60d5a28cfb51f88

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12903012457)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60.json)

### vs. 3.12.6

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-3.12.6.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.113x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-3.13.0rc2.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-3.13.0rc2.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.158x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-default_base_vs_NOGIL.svg)

### vs. base

- [🧠memory plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-base-mem.svg)
- [📄table](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-base.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-base.svg)

