# Results

- fork: python/180ee43bde99b8ce4c4f
- version: 3.14.0a4+
- config: 
- commit hash: [180ee43](https://github.com/python/cpython/commit/180ee43)
- commit date: 2025-01-28T12:40:44+01:00
- commit merge base: [4d0d24f6e3dff2864007c3cfd1cf7d49c6ee5317](https://github.com/python/cpython/commit/4d0d24f6e3dff2864007c3cfd1cf7d49c6ee5317)
- ref: 180ee43bde99b8ce4c4f

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13015139718)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43.json)

### vs. 3.12.6

- Geometric mean: 1.057x faster (HPT: reliability of 98.37%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43-vs-3.12.6.md)
- [📈time plot](bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x faster (HPT: reliability of 92.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43-vs-3.13.0rc2.md)
- [📈time plot](bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13015139718)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43-vs-3.12.6.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43-vs-3.13.0rc2.md)
- [📈time plot](bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4%2B-180ee43-vs-3.13.0rc2.svg)

