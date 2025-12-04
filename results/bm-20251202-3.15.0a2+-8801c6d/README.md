# Results

- fork: python/8801c6dec79275e9b588
- version: 3.15.0a2+
- config: 
- commit hash: [8801c6d](https://github.com/python/cpython/commit/8801c6d)
- commit date: 2025-12-02T20:33:40+00:00
- commit merge base: [d3c888b4ec15dbd7d6b6ef4f15b558af77c228af](https://github.com/python/cpython/commit/d3c888b4ec15dbd7d6b6ef4f15b558af77c228af)
- ref: 8801c6dec79275e9b588

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19878081757)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251202-vultr-x86_64-python-8801c6dec79275e9b588-3.15.0a2%2B-8801c6d.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251202-vultr-x86_64-python-8801c6dec79275e9b588-3.15.0a2%2B-8801c6d-vs-3.12.6.md)
- [📈time plot](bm-20251202-vultr-x86_64-python-8801c6dec79275e9b588-3.15.0a2%2B-8801c6d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251202-vultr-x86_64-python-8801c6dec79275e9b588-3.15.0a2%2B-8801c6d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251202-vultr-x86_64-python-8801c6dec79275e9b588-3.15.0a2%2B-8801c6d-vs-3.13.0rc2.svg)

