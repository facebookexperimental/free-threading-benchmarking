# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [fcfdb55](https://github.com/python/cpython/commit/fcfdb55)
- commit date: 2024-11-21T16:36:11-08:00
- commit merge base: [fd133d4f21cd7f5cbf6bcf332290ce52e5501167](https://github.com/python/cpython/commit/fd133d4f21cd7f5cbf6bcf332290ce52e5501167)
- ref: fcfdb55465636afc256b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11964316412)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55.json)

### vs. 3.12.6

- Geometric mean: 1.33x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.12.6.md)
- [📈time plot](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.38x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.13.0rc2.md)
- [📈time plot](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.39x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-base-mem.svg)
- [📄table](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-base.md)
- [📈time plot](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11964316412)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55.json)

### vs. 3.12.6

- Geometric mean: 1.46x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.12.6.md)
- [📈time plot](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.51x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.13.0rc2.md)
- [📈time plot](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.47x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-base-mem.svg)
- [📄table](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-base.md)
- [📈time plot](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-base.svg)

