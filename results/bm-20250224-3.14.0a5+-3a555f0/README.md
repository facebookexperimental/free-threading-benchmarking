# Results

- fork: python/3a555f09f387a0212e59
- version: 3.14.0a5+
- config: 
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

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)
- [📈time plot](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg)

