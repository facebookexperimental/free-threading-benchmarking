# Results

- fork: python/38642bff139bde5c0118
- version: 3.14.0a5+
- config: 
- commit hash: [38642bf](https://github.com/python/cpython/commit/38642bf)
- commit date: 2025-02-21T17:54:22+00:00
- commit merge base: [d88677ac20b9466387459d5adb2e87b7de64bc19](https://github.com/python/cpython/commit/d88677ac20b9466387459d5adb2e87b7de64bc19)
- ref: 38642bff139bde5c0118

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13467536316)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf.json)

### vs. 3.12.6

- Geometric mean: 1.064x faster (HPT: reliability of 99.50%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.md)
- [📈time plot](bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 92.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13467536316)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf.json)

### vs. 3.12.6

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.md)
- [📈time plot](bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.svg)

