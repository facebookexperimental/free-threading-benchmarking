# Results

- fork: python/0a6412f9cc9e694e7629
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [0a6412f](https://github.com/python/cpython/commit/0a6412f)
- commit date: 2025-01-20T17:03:44+00:00
- commit merge base: [38a99568763604ccec5d5027f0658100ad76876f](https://github.com/python/cpython/commit/38a99568763604ccec5d5027f0658100ad76876f)
- ref: 0a6412f9cc9e694e7629

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12894574940)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250120-vultr-x86_64-python-0a6412f9cc9e694e7629-3.14.0a4%2B-0a6412f.json)

### vs. 3.12.6

- Geometric mean: 1.052x slower (HPT: reliability of 99.96%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-0a6412f9cc9e694e7629-3.14.0a4%2B-0a6412f-vs-3.12.6.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-0a6412f9cc9e694e7629-3.14.0a4%2B-0a6412f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-0a6412f9cc9e694e7629-3.14.0a4%2B-0a6412f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-0a6412f9cc9e694e7629-3.14.0a4%2B-0a6412f-vs-3.13.0rc2.svg)

