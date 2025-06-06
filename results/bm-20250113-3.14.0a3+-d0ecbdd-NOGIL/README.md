# Results

- fork: python/d0ecbdd838034c1f061e
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [d0ecbdd](https://github.com/python/cpython/commit/d0ecbdd)
- commit date: 2025-01-13T07:09:39+08:00
- commit merge base: [5e65a1acc0b630397f1d190aed279114e6e99612](https://github.com/python/cpython/commit/5e65a1acc0b630397f1d190aed279114e6e99612)
- ref: d0ecbdd838034c1f061e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12738449067)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd.json)

### vs. 3.12.6

- Geometric mean: 1.162x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.189x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.233x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base-mem.svg)
- [📄table](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base.svg)

