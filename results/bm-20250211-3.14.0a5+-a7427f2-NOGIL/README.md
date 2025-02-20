# Results

- fork: python/a7427f2db937adb4c787
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [a7427f2](https://github.com/python/cpython/commit/a7427f2)
- commit date: 2025-02-11T17:29:27-05:00
- commit merge base: [1f233f56d6a5216b18e8c3f6b8c14d7e5d62c340](https://github.com/python/cpython/commit/1f233f56d6a5216b18e8c3f6b8c14d7e5d62c340)
- ref: a7427f2db937adb4c787

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13420918386)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5%2B-a7427f2.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.96%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5%2B-a7427f2-vs-3.12.6.md)
- [📈time plot](bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5%2B-a7427f2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5%2B-a7427f2-vs-3.13.0rc2.md)
- [📈time plot](bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5%2B-a7427f2-vs-3.13.0rc2.svg)

