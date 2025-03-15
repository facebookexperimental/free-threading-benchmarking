# Results

- fork: python/55815a6474c59001f023
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [55815a6](https://github.com/python/cpython/commit/55815a6)
- commit date: 2025-03-14T21:23:27+00:00
- commit merge base: [26511993e63265ea5928aabe6af96d89e20f0553](https://github.com/python/cpython/commit/26511993e63265ea5928aabe6af96d89e20f0553)
- ref: 55815a6474c59001f023

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13867522983)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 99.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)
- [📈time plot](bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 99.82%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg)

