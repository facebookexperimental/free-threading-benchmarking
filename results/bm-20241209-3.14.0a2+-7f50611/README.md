# Results

- fork: colesbury/mro
- version: 3.14.0a2+
- config: 
- commit hash: [7f50611](https://github.com/colesbury/cpython/commit/7f50611)
- commit date: 2024-12-09T19:19:59+00:00
- commit merge base: [5b6635f772d187d6049a56bfea76855644cd4ca1](https://github.com/python/cpython/commit/5b6635f772d187d6049a56bfea76855644cd4ca1)
- ref: mro

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12242759347)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2%2B-7f50611.json)

### vs. 3.12.6

- Geometric mean: 1.058x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2%2B-7f50611-vs-3.12.6.md)
- [📈time plot](bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2%2B-7f50611-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 71.13%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2%2B-7f50611-vs-3.13.0rc2.md)
- [📈time plot](bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2%2B-7f50611-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.009x slower (HPT: reliability of 95.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: 🔴 coverage, sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2%2B-7f50611-vs-base-mem.svg)
- [📄table](bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2%2B-7f50611-vs-base.md)
- [📈time plot](bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2%2B-7f50611-vs-base.svg)

