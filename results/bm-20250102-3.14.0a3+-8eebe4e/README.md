# Results

- fork: python/8eebe4e6d02bb4ad3f1c
- version: 3.14.0a3+
- config: 
- commit hash: [8eebe4e](https://github.com/python/cpython/commit/8eebe4e)
- commit date: 2025-01-02T14:02:54-05:00
- commit merge base: [c9356feef28e6dfc4dc32830d3427a5ae0e426e2](https://github.com/python/cpython/commit/c9356feef28e6dfc4dc32830d3427a5ae0e426e2)
- ref: 8eebe4e6d02bb4ad3f1c

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12590689759)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e.json)

### vs. 3.12.6

- Geometric mean: 1.145x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.12.6.md)
- [📈time plot](bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12590689759)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e.json)

### vs. 3.12.6

- Geometric mean: 1.095x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.12.6.md)
- [📈time plot](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3%2B-8eebe4e-vs-3.13.0rc2.svg)

