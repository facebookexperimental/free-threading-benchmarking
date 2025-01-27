# Results

- fork: python/a8dc6d6d44a141a8f839
- version: 3.14.0a4+
- config: 
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

- Geometric mean: 1.121x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.md)
- [📈time plot](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12979733746)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.md)
- [📈time plot](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.svg)

