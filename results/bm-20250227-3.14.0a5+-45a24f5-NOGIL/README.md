# Results

- fork: python/45a24f54af4a65c14cc1
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [45a24f5](https://github.com/python/cpython/commit/45a24f5)
- commit date: 2025-02-27T12:51:47+00:00
- commit merge base: [a083633fa046386b8cdaae0c87fef25289dde9a1](https://github.com/python/cpython/commit/a083633fa046386b8cdaae0c87fef25289dde9a1)
- ref: 45a24f54af4a65c14cc1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13595814277)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5%2B-45a24f5.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5%2B-45a24f5-vs-3.12.6.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5%2B-45a24f5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5%2B-45a24f5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5%2B-45a24f5-vs-3.13.0rc2.svg)

