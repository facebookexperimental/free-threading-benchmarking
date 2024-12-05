# Results

- fork: colesbury/gh_127582_resurrecti
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [a7b41c8](https://github.com/colesbury/cpython/commit/a7b41c8)
- commit date: 2024-12-04T19:01:42+00:00
- commit merge base: [6bc3e830a518112a4e242217807681e3908602f4](https://github.com/python/cpython/commit/6bc3e830a518112a4e242217807681e3908602f4)
- ref: gh_127582_resurrecti

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12170581606)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2%2B-a7b41c8.json)

### vs. 3.12.6

- Geometric mean: 1.225x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2%2B-a7b41c8-vs-3.12.6.md)
- [📈time plot](bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2%2B-a7b41c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.249x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2%2B-a7b41c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2%2B-a7b41c8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 80.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2%2B-a7b41c8-vs-base-mem.svg)
- [📄table](bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2%2B-a7b41c8-vs-base.md)
- [📈time plot](bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2%2B-a7b41c8-vs-base.svg)

