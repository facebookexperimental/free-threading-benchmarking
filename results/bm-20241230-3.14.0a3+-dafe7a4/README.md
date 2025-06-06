# Results

- fork: python/dafe7a44630aa32bb411
- version: 3.14.0a3+
- config: 
- commit hash: [dafe7a4](https://github.com/python/cpython/commit/dafe7a4)
- commit date: 2024-12-30T20:52:04+00:00
- commit merge base: [47d2cb8eb7595df5940225867dbb66b6dd59413a](https://github.com/python/cpython/commit/47d2cb8eb7595df5940225867dbb66b6dd59413a)
- ref: dafe7a44630aa32bb411

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12553563219)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.md)
- [📈time plot](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.svg)

