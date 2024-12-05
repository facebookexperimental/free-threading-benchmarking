# Results

- fork: python/d24a22e9b6377797c3b6
- version: 3.14.0a2+
- config: 
- commit hash: [d24a22e](https://github.com/python/cpython/commit/d24a22e)
- commit date: 2024-11-22T12:07:05-08:00
- commit merge base: [4b12a6ff4ac6659156a01ae224249c7e145ff865](https://github.com/python/cpython/commit/4b12a6ff4ac6659156a01ae224249c7e145ff865)
- ref: d24a22e9b6377797c3b6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11981825901)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.12.6.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 90.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.13.0rc2.svg)

