# Results

- fork: python/78ffba4221dcb2e39fd5
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [78ffba4](https://github.com/python/cpython/commit/78ffba4)
- commit date: 2024-12-20T14:28:18+01:00
- commit merge base: [ba45e5cdd41a39ce0b3de08bdcfa9d8e28e0e4f3](https://github.com/python/cpython/commit/ba45e5cdd41a39ce0b3de08bdcfa9d8e28e0e4f3)
- ref: 78ffba4221dcb2e39fd5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12434814924)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3%2B-78ffba4.json)

### vs. 3.12.6

- Geometric mean: 1.188x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3%2B-78ffba4-vs-3.12.6.md)
- [📈time plot](bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3%2B-78ffba4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.215x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3%2B-78ffba4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3%2B-78ffba4-vs-3.13.0rc2.svg)

