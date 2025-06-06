# Results

- fork: python/c84928ed6de105696be2
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [c84928e](https://github.com/python/cpython/commit/c84928e)
- commit date: 2024-12-11T15:18:22-08:00
- commit merge base: [e8f4e272cc828f2b79fa17fc6b9786bdddab7ce4](https://github.com/python/cpython/commit/e8f4e272cc828f2b79fa17fc6b9786bdddab7ce4)
- ref: c84928ed6de105696be2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12287367377)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241211-vultr-x86_64-python-c84928ed6de105696be2-3.14.0a2%2B-c84928e.json)

### vs. 3.12.6

- Geometric mean: 1.220x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241211-vultr-x86_64-python-c84928ed6de105696be2-3.14.0a2%2B-c84928e-vs-3.12.6.md)
- [📈time plot](bm-20241211-vultr-x86_64-python-c84928ed6de105696be2-3.14.0a2%2B-c84928e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.244x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241211-vultr-x86_64-python-c84928ed6de105696be2-3.14.0a2%2B-c84928e-vs-3.13.0rc2.md)
- [📈time plot](bm-20241211-vultr-x86_64-python-c84928ed6de105696be2-3.14.0a2%2B-c84928e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.276x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241211-vultr-x86_64-python-c84928ed6de105696be2-3.14.0a2%2B-c84928e-vs-base-mem.svg)
- [📄table](bm-20241211-vultr-x86_64-python-c84928ed6de105696be2-3.14.0a2%2B-c84928e-vs-base.md)
- [📈time plot](bm-20241211-vultr-x86_64-python-c84928ed6de105696be2-3.14.0a2%2B-c84928e-vs-base.svg)

