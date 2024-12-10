# Results

- fork: python/5c89adf385aaaca97c2e
- version: 3.14.0a2+
- config: 
- commit hash: [5c89adf](https://github.com/python/cpython/commit/5c89adf)
- commit date: 2024-12-09T18:31:22+00:00
- commit merge base: [e85f2f1703e0f79cfd0d0e3010190b71c0eb18da](https://github.com/python/cpython/commit/e85f2f1703e0f79cfd0d0e3010190b71c0eb18da)
- ref: 5c89adf385aaaca97c2e

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12246883169)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf.json)

### vs. 3.12.6

- Geometric mean: 1.119x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf-vs-3.12.6.md)
- [📈time plot](bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf-vs-3.13.0rc2.md)
- [📈time plot](bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12246883169)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf.json)

### vs. 3.12.6

- Geometric mean: 1.060x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf-vs-3.12.6.md)
- [📈time plot](bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 92.50%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf-vs-3.13.0rc2.md)
- [📈time plot](bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2%2B-5c89adf-vs-3.13.0rc2.svg)

