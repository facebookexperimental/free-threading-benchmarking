# Results

- fork: python/79b7cab50a3292a1c014
- version: 3.14.0a2+
- config: 
- commit hash: [79b7cab](https://github.com/python/cpython/commit/79b7cab)
- commit date: 2024-12-07T17:58:42+00:00
- commit merge base: [27d0d2141319d82709eb09ba20065df3e1714fab](https://github.com/python/cpython/commit/27d0d2141319d82709eb09ba20065df3e1714fab)
- ref: 79b7cab50a3292a1c014

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12217207993)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20241207-vultr-x86_64-python-79b7cab50a3292a1c014-3.14.0a2%2B-79b7cab-pystats.json)
- [pystats table](bm-20241207-vultr-x86_64-python-79b7cab50a3292a1c014-3.14.0a2%2B-79b7cab-pystats.md)
- [raw results](bm-20241207-vultr-x86_64-python-79b7cab50a3292a1c014-3.14.0a2%2B-79b7cab.json)

### vs. 3.12.6

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241207-vultr-x86_64-python-79b7cab50a3292a1c014-3.14.0a2%2B-79b7cab-vs-3.12.6.md)
- [📈time plot](bm-20241207-vultr-x86_64-python-79b7cab50a3292a1c014-3.14.0a2%2B-79b7cab-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 97.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241207-vultr-x86_64-python-79b7cab50a3292a1c014-3.14.0a2%2B-79b7cab-vs-3.13.0rc2.md)
- [📈time plot](bm-20241207-vultr-x86_64-python-79b7cab50a3292a1c014-3.14.0a2%2B-79b7cab-vs-3.13.0rc2.svg)

