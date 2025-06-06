# Results

- fork: python/7e6ee50b6b8c760bcefb
- version: 3.14.0a4+
- config: 
- commit hash: [7e6ee50](https://github.com/python/cpython/commit/7e6ee50)
- commit date: 2025-02-10T00:27:28+01:00
- commit merge base: [d05053a203d922c8056f12ef3c9338229fdce043](https://github.com/python/cpython/commit/d05053a203d922c8056f12ef3c9338229fdce043)
- ref: 7e6ee50b6b8c760bcefb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13231062426)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)
- [📈time plot](bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)
- [📈time plot](bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg)

