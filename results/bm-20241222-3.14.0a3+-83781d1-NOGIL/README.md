# Results

- fork: colesbury/align_32
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [83781d1](https://github.com/colesbury/cpython/commit/83781d1)
- commit date: 2024-12-22T17:17:01+00:00
- commit merge base: [f420bdd29fbc1a97ad20d88075c38c937c1f8479](https://github.com/python/cpython/commit/f420bdd29fbc1a97ad20d88075c38c937c1f8479)
- ref: align_32

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12456412425)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1.json)

### vs. 3.12.6

- Geometric mean: 1.177x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-3.12.6.md)
- [📈time plot](bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.203x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-3.13.0rc2.md)
- [📈time plot](bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-base-mem.svg)
- [📄table](bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-base.md)
- [📈time plot](bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-base.svg)

