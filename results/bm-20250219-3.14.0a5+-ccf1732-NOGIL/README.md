# Results

- fork: python/ccf17323c218a2fdcf7f
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [ccf1732](https://github.com/python/cpython/commit/ccf1732)
- commit date: 2025-02-19T12:11:17-05:00
- commit merge base: [5f00501a940a0fb97870e70066fb301909320388](https://github.com/python/cpython/commit/5f00501a940a0fb97870e70066fb301909320388)
- ref: ccf17323c218a2fdcf7f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13419877451)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5%2B-ccf1732.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 99.98%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5%2B-ccf1732-vs-3.12.6.md)
- [📈time plot](bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5%2B-ccf1732-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5%2B-ccf1732-vs-3.13.0rc2.md)
- [📈time plot](bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5%2B-ccf1732-vs-3.13.0rc2.svg)

