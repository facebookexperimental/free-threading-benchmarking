# Results

- fork: python/ea2b53739f1128184b41
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [ea2b537](https://github.com/python/cpython/commit/ea2b537)
- commit date: 2024-12-26T13:53:37-08:00
- commit merge base: [3bd7730bbda3e38db5920a7b8c95958ca90342bf](https://github.com/python/cpython/commit/3bd7730bbda3e38db5920a7b8c95958ca90342bf)
- ref: ea2b53739f1128184b41

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12509857094)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537.json)

### vs. 3.12.6

- Geometric mean: 1.162x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.md)
- [📈time plot](bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.189x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.md)
- [📈time plot](bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.228x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base-mem.svg)
- [📄table](bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base.md)
- [📈time plot](bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base.svg)

