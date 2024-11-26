# Results

- fork: python
- version: 3.14.0a2+
- config: 
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

- Geometric mean: 1.081x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.12.6.md)
- [📈time plot](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.13.0rc2.md)
- [📈time plot](bm-20241121-linux-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11964316412)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55.json)

### vs. 3.12.6

- Geometric mean: 1.042x faster (HPT: reliability of 99.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.12.6.md)
- [📈time plot](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x faster (HPT: reliability of 67.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.13.0rc2.md)
- [📈time plot](bm-20241121-vultr-x86_64-python-fcfdb55465636afc256b-3.14.0a2%2B-fcfdb55-vs-3.13.0rc2.svg)

