# Results

- fork: python/9d3a8f494985e8bbef69
- version: 3.14.0a3+
- config: 
- commit hash: [9d3a8f4](https://github.com/python/cpython/commit/9d3a8f4)
- commit date: 2024-12-22T11:01:45-08:00
- commit merge base: [f420bdd29fbc1a97ad20d88075c38c937c1f8479](https://github.com/python/cpython/commit/f420bdd29fbc1a97ad20d88075c38c937c1f8479)
- ref: 9d3a8f494985e8bbef69

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12458964992)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.md)
- [📈time plot](bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12458964992)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.md)
- [📈time plot](bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.svg)

