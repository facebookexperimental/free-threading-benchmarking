# Results

- fork: python/5e73ece95e8aa92d0695
- version: 3.14.0a5+
- config: 
- commit hash: [5e73ece](https://github.com/python/cpython/commit/5e73ece)
- commit date: 2025-03-05T22:59:56+00:00
- commit merge base: [1b5db5adfec10d90cf5c7abd6817452be4f0b909](https://github.com/python/cpython/commit/1b5db5adfec10d90cf5c7abd6817452be4f0b909)
- ref: 5e73ece95e8aa92d0695

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13688332448)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250305-vultr-x86_64-python-5e73ece95e8aa92d0695-3.14.0a5%2B-5e73ece.json)

### vs. 3.12.6

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250305-vultr-x86_64-python-5e73ece95e8aa92d0695-3.14.0a5%2B-5e73ece-vs-3.12.6.md)
- [📈time plot](bm-20250305-vultr-x86_64-python-5e73ece95e8aa92d0695-3.14.0a5%2B-5e73ece-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250305-vultr-x86_64-python-5e73ece95e8aa92d0695-3.14.0a5%2B-5e73ece-vs-3.13.0rc2.md)
- [📈time plot](bm-20250305-vultr-x86_64-python-5e73ece95e8aa92d0695-3.14.0a5%2B-5e73ece-vs-3.13.0rc2.svg)

