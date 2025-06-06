# Results

- fork: python/61b35f74aa4a6ac60663
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [61b35f7](https://github.com/python/cpython/commit/61b35f7)
- commit date: 2025-01-18T16:53:06-05:00
- commit merge base: [e8092e5cdcd6707ac0b16d8fb37fa080a88bcc97](https://github.com/python/cpython/commit/e8092e5cdcd6707ac0b16d8fb37fa080a88bcc97)
- ref: 61b35f74aa4a6ac60663

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12848571184)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7.json)

### vs. 3.12.6

- Geometric mean: 1.055x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.12.6.md)
- [📈time plot](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.13.0rc2.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.139x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, html5lib, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-default_base_vs_NOGIL.svg)

