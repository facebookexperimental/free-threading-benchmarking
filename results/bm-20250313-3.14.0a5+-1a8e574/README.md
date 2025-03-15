# Results

- fork: python/1a8e5742cdcf3dba7fc5
- version: 3.14.0a5+
- config: 
- commit hash: [1a8e574](https://github.com/python/cpython/commit/1a8e574)
- commit date: 2025-03-13T22:54:17+03:00
- commit merge base: [ec46a55d63eaf015c2cd544b8c727ed7cbb81d33](https://github.com/python/cpython/commit/ec46a55d63eaf015c2cd544b8c727ed7cbb81d33)
- ref: 1a8e5742cdcf3dba7fc5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13867391541)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574.json)

### vs. 3.12.6

- Geometric mean: 1.060x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.12.6.md)
- [📈time plot](bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 77.45%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.13.0rc2.md)
- [📈time plot](bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.13.0rc2.svg)

