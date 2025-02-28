# Results

- fork: python/9211b3dabeacb92713ac
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [9211b3d](https://github.com/python/cpython/commit/9211b3d)
- commit date: 2025-02-28T07:33:10+08:00
- commit merge base: [6140b0896e95ca96aa15472e14d0502966391485](https://github.com/python/cpython/commit/6140b0896e95ca96aa15472e14d0502966391485)
- ref: 9211b3dabeacb92713ac

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13578567493)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d.json)

### vs. 3.12.6

- Geometric mean: 1.005x slower (HPT: reliability of 99.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.md)
- [📈time plot](bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x slower (HPT: reliability of 99.75%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base-mem.svg)
- [📄table](bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base.md)
- [📈time plot](bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13578567493)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d.json)

### vs. 3.12.6

- Geometric mean: 1.057x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.150x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base-mem.svg)
- [📄table](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base.svg)

