# Results

- fork: python/1c3bb200da77f9df30af
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [1c3bb20](https://github.com/python/cpython/commit/1c3bb20)
- commit date: 2025-01-28T01:12:45+01:00
- commit merge base: [379ab856f59423c570333403a7d5d72f3ea82d52](https://github.com/python/cpython/commit/379ab856f59423c570333403a7d5d72f3ea82d52)
- ref: 1c3bb200da77f9df30af

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13001011446)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20.json)

### vs. 3.12.6

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.md)
- [📈time plot](bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.131x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.md)
- [📈time plot](bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.152x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base-mem.svg)
- [📄table](bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base.md)
- [📈time plot](bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13001011446)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20.json)

### vs. 3.12.6

- Geometric mean: 1.077x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.153x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base-mem.svg)
- [📄table](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base.svg)

