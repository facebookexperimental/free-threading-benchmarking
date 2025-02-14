# Results

- fork: python/07f5e33f2eed50984d7a
- version: 3.14.0a5+
- config: 
- commit hash: [07f5e33](https://github.com/python/cpython/commit/07f5e33)
- commit date: 2025-02-13T17:29:26+00:00
- commit merge base: [451f291baaff918228ace4e8257be42737d7654a](https://github.com/python/cpython/commit/451f291baaff918228ace4e8257be42737d7654a)
- ref: 07f5e33f2eed50984d7a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13321898154)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5%2B-07f5e33.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5%2B-07f5e33-vs-3.12.6.md)
- [📈time plot](bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5%2B-07f5e33-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5%2B-07f5e33-vs-3.13.0rc2.md)
- [📈time plot](bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5%2B-07f5e33-vs-3.13.0rc2.svg)

