# Results

- fork: python/29caec62ee0650493c83
- version: 3.14.0a4+
- config: 
- commit hash: [29caec6](https://github.com/python/cpython/commit/29caec6)
- commit date: 2025-01-21T21:06:13+00:00
- commit merge base: [5a9afe23620aadea30013076d64686be8bf66f7e](https://github.com/python/cpython/commit/5a9afe23620aadea30013076d64686be8bf66f7e)
- ref: 29caec62ee0650493c83

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12903010477)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4%2B-29caec6.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4%2B-29caec6-vs-3.12.6.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4%2B-29caec6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4%2B-29caec6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4%2B-29caec6-vs-3.13.0rc2.svg)

