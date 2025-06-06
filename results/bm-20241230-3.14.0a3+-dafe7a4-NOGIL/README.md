# Results

- fork: python/dafe7a44630aa32bb411
- version: 3.14.0a3+
- config: NOGIL
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

- Geometric mean: 1.168x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.md)
- [📈time plot](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.194x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.233x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base-mem.svg)
- [📄table](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base.md)
- [📈time plot](bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base.svg)

