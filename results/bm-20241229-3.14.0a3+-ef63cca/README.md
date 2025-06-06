# Results

- fork: python/ef63cca494571f50906b
- version: 3.14.0a3+
- config: 
- commit hash: [ef63cca](https://github.com/python/cpython/commit/ef63cca)
- commit date: 2024-12-29T22:07:12+00:00
- commit merge base: [c78729f2df7c0e220f1080edb2a0d0cdd49e22df](https://github.com/python/cpython/commit/c78729f2df7c0e220f1080edb2a0d0cdd49e22df)
- ref: ef63cca494571f50906b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12539938547)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241229-vultr-x86_64-python-ef63cca494571f50906b-3.14.0a3%2B-ef63cca.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241229-vultr-x86_64-python-ef63cca494571f50906b-3.14.0a3%2B-ef63cca-vs-3.12.6.md)
- [📈time plot](bm-20241229-vultr-x86_64-python-ef63cca494571f50906b-3.14.0a3%2B-ef63cca-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241229-vultr-x86_64-python-ef63cca494571f50906b-3.14.0a3%2B-ef63cca-vs-3.13.0rc2.md)
- [📈time plot](bm-20241229-vultr-x86_64-python-ef63cca494571f50906b-3.14.0a3%2B-ef63cca-vs-3.13.0rc2.svg)

