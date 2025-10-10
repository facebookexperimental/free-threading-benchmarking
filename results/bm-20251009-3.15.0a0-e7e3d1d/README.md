# Results

- fork: python/e7e3d1d4a8dece01b1bb
- version: 3.15.0a0
- config: 
- commit hash: [e7e3d1d](https://github.com/python/cpython/commit/e7e3d1d)
- commit date: 2025-10-09T00:34:40+02:00
- commit merge base: [678e0b818c0d6063907f55263bbc0e194b492c8e](https://github.com/python/cpython/commit/678e0b818c0d6063907f55263bbc0e194b492c8e)
- ref: e7e3d1d4a8dece01b1bb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18361703290)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.12.6.md)
- [📈time plot](bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.13.0rc2.svg)

