# Results

- fork: python/a549f439384b4509b256
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [a549f43](https://github.com/python/cpython/commit/a549f43)
- commit date: 2025-01-30T00:02:31+00:00
- commit merge base: [99849ee0d3ebcddc97b6aeaf389f43a12f541068](https://github.com/python/cpython/commit/99849ee0d3ebcddc97b6aeaf389f43a12f541068)
- ref: a549f439384b4509b256

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13043049408)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43.json)

### vs. 3.12.6

- Geometric mean: 1.045x slower (HPT: reliability of 99.95%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.md)
- [📈time plot](bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.md)
- [📈time plot](bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.134x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base-mem.svg)
- [📄table](bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base.md)
- [📈time plot](bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base.svg)

