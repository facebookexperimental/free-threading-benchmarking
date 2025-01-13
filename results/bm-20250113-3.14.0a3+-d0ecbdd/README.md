# Results

- fork: python/d0ecbdd838034c1f061e
- version: 3.14.0a3+
- config: 
- commit hash: [d0ecbdd](https://github.com/python/cpython/commit/d0ecbdd)
- commit date: 2025-01-13T07:09:39+08:00
- commit merge base: [5e65a1acc0b630397f1d190aed279114e6e99612](https://github.com/python/cpython/commit/5e65a1acc0b630397f1d190aed279114e6e99612)
- ref: d0ecbdd838034c1f061e

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12738449067)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.md)
- [📈time plot](bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 98.65%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12738449067)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.svg)

