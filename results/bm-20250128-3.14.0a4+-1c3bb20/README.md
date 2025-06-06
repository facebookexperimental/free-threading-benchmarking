# Results

- fork: python/1c3bb200da77f9df30af
- version: 3.14.0a4+
- config: 
- commit hash: [1c3bb20](https://github.com/python/cpython/commit/1c3bb20)
- commit date: 2025-01-28T01:12:45+01:00
- commit merge base: [379ab856f59423c570333403a7d5d72f3ea82d52](https://github.com/python/cpython/commit/379ab856f59423c570333403a7d5d72f3ea82d52)
- ref: 1c3bb200da77f9df30af

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13001011446)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.svg)

