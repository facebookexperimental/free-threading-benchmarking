# Results

- fork: python/75b628adebd4594529da
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [75b628a](https://github.com/python/cpython/commit/75b628a)
- commit date: 2025-02-03T15:09:21+00:00
- commit merge base: [808071b994370886a169cfb97cef1ca3837f89c1](https://github.com/python/cpython/commit/808071b994370886a169cfb97cef1ca3837f89c1)
- ref: 75b628adebd4594529da

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13142865732)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-3.12.6.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.016x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-base-mem.svg)
- [📄table](bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-base.md)
- [📈time plot](bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-base.svg)

