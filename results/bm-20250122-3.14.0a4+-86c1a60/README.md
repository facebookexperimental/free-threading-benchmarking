# Results

- fork: python/86c1a60d5a28cfb51f88
- version: 3.14.0a4+
- config: 
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

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-3.12.6.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-3.13.0rc2.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 96.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-base-mem.svg)
- [📄table](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-base.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-86c1a60d5a28cfb51f88-3.14.0a4%2B-86c1a60-vs-base.svg)

