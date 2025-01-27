# Results

- fork: python/a8dc6d6d44a141a8f839
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [a8dc6d6](https://github.com/python/cpython/commit/a8dc6d6)
- commit date: 2025-01-26T19:00:28+00:00
- commit merge base: [914c232e9391e8e5014b089ba12c75d4a3b0cc7f](https://github.com/python/cpython/commit/914c232e9391e8e5014b089ba12c75d4a3b0cc7f)
- ref: a8dc6d6d44a141a8f839

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12979733746)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 99.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.md)
- [📈time plot](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 99.95%, 1.02x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.136x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base-mem.svg)
- [📄table](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base.md)
- [📈time plot](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12979733746)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6.json)

### vs. 3.12.6

- Geometric mean: 1.059x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.md)
- [📈time plot](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.089x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.135x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base-mem.svg)
- [📄table](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base.md)
- [📈time plot](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base.svg)

