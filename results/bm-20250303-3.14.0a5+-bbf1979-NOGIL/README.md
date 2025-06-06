# Results

- fork: python/bbf197913ca984b79fee
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [bbf1979](https://github.com/python/cpython/commit/bbf1979)
- commit date: 2025-03-03T14:58:33-08:00
- commit merge base: [3a7f17c7e2f72a836a019c316818c446a0c71d75](https://github.com/python/cpython/commit/3a7f17c7e2f72a836a019c316818c446a0c71d75)
- ref: bbf197913ca984b79fee

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13643350016)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.12.6.md)
- [📈time plot](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.13.0rc2.md)
- [📈time plot](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.139x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-base-mem.svg)
- [📄table](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-base.md)
- [📈time plot](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-base.svg)

