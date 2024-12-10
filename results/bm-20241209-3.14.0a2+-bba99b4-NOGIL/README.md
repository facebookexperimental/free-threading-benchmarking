# Results

- fork: colesbury/stackpointer
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [bba99b4](https://github.com/colesbury/cpython/commit/bba99b4)
- commit date: 2024-12-09T21:56:08+00:00
- commit merge base: [5c89adf385aaaca97c2ee9074f8b1fda0f57ad26](https://github.com/python/cpython/commit/5c89adf385aaaca97c2ee9074f8b1fda0f57ad26)
- ref: stackpointer

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12245093641)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2%2B-bba99b4.json)

### vs. 3.12.6

- Geometric mean: 1.234x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2%2B-bba99b4-vs-3.12.6.md)
- [📈time plot](bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2%2B-bba99b4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.259x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2%2B-bba99b4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2%2B-bba99b4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2%2B-bba99b4-vs-base-mem.svg)
- [📄table](bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2%2B-bba99b4-vs-base.md)
- [📈time plot](bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2%2B-bba99b4-vs-base.svg)

