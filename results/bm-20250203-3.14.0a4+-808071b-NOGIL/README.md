# Results

- fork: python/808071b994370886a169
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [808071b](https://github.com/python/cpython/commit/808071b)
- commit date: 2025-02-03T12:41:32+00:00
- commit merge base: [218f205f2091cb173b5fe3f4b265c102cdf093b3](https://github.com/python/cpython/commit/218f205f2091cb173b5fe3f4b265c102cdf093b3)
- ref: 808071b994370886a169

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13142865732)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 99.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b-vs-3.12.6.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 99.90%, 1.02x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b-vs-3.13.0rc2.svg)

