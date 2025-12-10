# Results

- fork: faster-cpython/tier_2_tos_caching
- version: 3.15.0a2+
- config: JIT
- commit hash: [4b24c15](https://github.com/faster%2dcpython/cpython/commit/4b24c15)
- commit date: 2025-12-10T17:06:40+00:00
- commit merge base: [46295677a13f141b8d52cc36202384554adba65d](https://github.com/python/cpython/commit/46295677a13f141b8d52cc36202384554adba65d)
- ref: tier_2_tos_caching

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20111389432)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251210-vultr-x86_64-faster%252dcpython-tier_2_tos_caching-3.15.0a2%2B-4b24c15.json)

### vs. 3.12.6

- Geometric mean: 1.108x faster (HPT: reliability of 99.99%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251210-vultr-x86_64-faster%252dcpython-tier_2_tos_caching-3.15.0a2%2B-4b24c15-vs-3.12.6.md)
- [📈time plot](bm-20251210-vultr-x86_64-faster%252dcpython-tier_2_tos_caching-3.15.0a2%2B-4b24c15-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x faster (HPT: reliability of 99.99%, 1.03x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251210-vultr-x86_64-faster%252dcpython-tier_2_tos_caching-3.15.0a2%2B-4b24c15-vs-3.13.0rc2.md)
- [📈time plot](bm-20251210-vultr-x86_64-faster%252dcpython-tier_2_tos_caching-3.15.0a2%2B-4b24c15-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 55.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: 🔴 docutils
- [🧠memory plot](bm-20251210-vultr-x86_64-faster%252dcpython-tier_2_tos_caching-3.15.0a2%2B-4b24c15-vs-base-mem.svg)
- [📄table](bm-20251210-vultr-x86_64-faster%252dcpython-tier_2_tos_caching-3.15.0a2%2B-4b24c15-vs-base.md)
- [📈time plot](bm-20251210-vultr-x86_64-faster%252dcpython-tier_2_tos_caching-3.15.0a2%2B-4b24c15-vs-base.svg)

