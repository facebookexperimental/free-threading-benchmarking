# Results

- fork: python/e991ac8f2037d78140e4
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [e991ac8](https://github.com/python/cpython/commit/e991ac8)
- commit date: 2024-12-06T10:03:03+05:30
- commit merge base: [25eee578c8e369b027da6d9d2725f29df6ef1cbd](https://github.com/python/cpython/commit/25eee578c8e369b027da6d9d2725f29df6ef1cbd)
- ref: e991ac8f2037d78140e4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12193934508)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2%2B-e991ac8.json)

### vs. 3.12.6

- Geometric mean: 1.223x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2%2B-e991ac8-vs-3.12.6.md)
- [📈time plot](bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2%2B-e991ac8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.247x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2%2B-e991ac8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2%2B-e991ac8-vs-3.13.0rc2.svg)

