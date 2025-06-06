# Results

- fork: python/3a555f09f387a0212e59
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [3a555f0](https://github.com/python/cpython/commit/3a555f0)
- commit date: 2025-02-24T21:35:00+00:00
- commit merge base: [78e09a488d41066dea5f8dcf22405a0d5dd8be23](https://github.com/python/cpython/commit/78e09a488d41066dea5f8dcf22405a0d5dd8be23)
- ref: 3a555f09f387a0212e59

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13510756979)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)
- [📈time plot](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.119x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base-mem.svg)
- [📄table](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.md)
- [📈time plot](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.svg)

