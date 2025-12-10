# Results

- fork: python/46295677a13f141b8d52
- version: 3.15.0a2+
- config: JIT
- commit hash: [4629567](https://github.com/python/cpython/commit/4629567)
- commit date: 2025-12-10T16:04:04+00:00
- commit merge base: [785268fdceb0d0fe217aed1d6e43e0231c0e50c3](https://github.com/python/cpython/commit/785268fdceb0d0fe217aed1d6e43e0231c0e50c3)
- ref: 46295677a13f141b8d52

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20111389432)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2%2B-4629567.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 99.99%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2%2B-4629567-vs-3.12.6.md)
- [📈time plot](bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2%2B-4629567-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2%2B-4629567-vs-3.13.0rc2.md)
- [📈time plot](bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2%2B-4629567-vs-3.13.0rc2.svg)

