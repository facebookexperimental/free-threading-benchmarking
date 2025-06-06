# Results

- fork: python/cf4c4ecc26c7e3b89f2e
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [cf4c4ec](https://github.com/python/cpython/commit/cf4c4ec)
- commit date: 2025-02-01T18:49:45+02:00
- commit merge base: [71ae93374defd192e5e88fe0912eff4f8e56f286](https://github.com/python/cpython/commit/71ae93374defd192e5e88fe0912eff4f8e56f286)
- ref: cf4c4ecc26c7e3b89f2e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13093073750)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 99.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.md)
- [📈time plot](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 99.92%, 1.02x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.md)
- [📈time plot](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- new benchmarks: html5lib
- [🧠memory plot](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base-mem.svg)
- [📄table](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base.md)
- [📈time plot](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base.svg)

