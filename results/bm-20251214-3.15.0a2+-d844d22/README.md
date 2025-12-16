# Results

- fork: python/d844d22cb00e4a8a224a
- version: 3.15.0a2+
- config: 
- commit hash: [d844d22](https://github.com/python/cpython/commit/d844d22)
- commit date: 2025-12-14T21:23:38+00:00
- commit merge base: [3f56186a2d0e22f4f279b0cd071e871a312e2c67](https://github.com/python/cpython/commit/3f56186a2d0e22f4f279b0cd071e871a312e2c67)
- ref: d844d22cb00e4a8a224a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20216709503)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.12.6.md)
- [📈time plot](bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.13.0rc2.md)
- [📈time plot](bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.13.0rc2.svg)

