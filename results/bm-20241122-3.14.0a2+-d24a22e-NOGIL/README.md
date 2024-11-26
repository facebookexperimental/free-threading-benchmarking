# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [d24a22e](https://github.com/python/cpython/commit/d24a22e)
- commit date: 2024-11-22T12:07:05-08:00
- commit merge base: [4b12a6ff4ac6659156a01ae224249c7e145ff865](https://github.com/python/cpython/commit/4b12a6ff4ac6659156a01ae224249c7e145ff865)
- ref: d24a22e9b6377797c3b6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11981215498)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e.json)

### vs. 3.12.6

- Geometric mean: 1.263x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.12.6.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.287x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.282x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-base-mem.svg)
- [📄table](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-base.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-base.svg)

