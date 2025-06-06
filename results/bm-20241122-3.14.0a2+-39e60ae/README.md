# Results

- fork: python/39e60aeb3837f1f23d8b
- version: 3.14.0a2+
- config: 
- commit hash: [39e60ae](https://github.com/python/cpython/commit/39e60ae)
- commit date: 2024-11-22T16:02:51-08:00
- commit merge base: [d24a22e9b6377797c3b602945347096fbe065670](https://github.com/python/cpython/commit/d24a22e9b6377797c3b602945347096fbe065670)
- ref: 39e60aeb3837f1f23d8b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11982244918)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.46%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 96.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 96.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base-mem.svg)
- [📄table](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.svg)

