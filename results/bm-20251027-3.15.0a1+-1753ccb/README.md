# Results

- fork: python/1753ccb43223b0a1054a
- version: 3.15.0a1+
- config: 
- commit hash: [1753ccb](https://github.com/python/cpython/commit/1753ccb)
- commit date: 2025-10-27T16:37:37+00:00
- commit merge base: [e03d8e4f509f3588c4f13e04006266100ddec0b2](https://github.com/python/cpython/commit/e03d8e4f509f3588c4f13e04006266100ddec0b2)
- ref: 1753ccb43223b0a1054a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19966284139)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1%2B-1753ccb.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1%2B-1753ccb-vs-3.12.6.md)
- [📈time plot](bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1%2B-1753ccb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.041x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1%2B-1753ccb-vs-3.13.0rc2.md)
- [📈time plot](bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1%2B-1753ccb-vs-3.13.0rc2.svg)

