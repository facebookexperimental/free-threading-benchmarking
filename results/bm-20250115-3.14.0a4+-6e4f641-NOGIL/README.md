# Results

- fork: python/6e4f64109b0eb6c9f1b5
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [6e4f641](https://github.com/python/cpython/commit/6e4f641)
- commit date: 2025-01-15T10:49:02+09:00
- commit merge base: [bd3baa8b1a7755f17b2fc98c7fb7b872fec43af3](https://github.com/python/cpython/commit/bd3baa8b1a7755f17b2fc98c7fb7b872fec43af3)
- ref: 6e4f64109b0eb6c9f1b5

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12782396272)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641.json)

### vs. 3.12.6

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.md)
- [📈time plot](bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.128x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.148x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base-mem.svg)
- [📄table](bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base.md)
- [📈time plot](bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12782396272)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641.json)

### vs. 3.12.6

- Geometric mean: 1.059x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.089x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.153x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base-mem.svg)
- [📄table](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base.svg)

