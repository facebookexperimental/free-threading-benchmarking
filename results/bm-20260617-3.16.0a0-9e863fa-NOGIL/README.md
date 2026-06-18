# Results

- fork: python/9e863fab283eddca9c2a
- version: 3.16.0a0
- config: NOGIL
- commit hash: [9e863fa](https://github.com/python/cpython/commit/9e863fa)
- commit date: 2026-06-17T00:16:06+01:00
- commit merge base: [c2ca7724af94df6e078a4b2e86d1be8c410d9940](https://github.com/python/cpython/commit/c2ca7724af94df6e078a4b2e86d1be8c410d9940)
- ref: 9e863fab283eddca9c2a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27658899681)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 89.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa-vs-3.12.6.md)
- [📈time plot](bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 97.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa-vs-3.13.0rc2.md)
- [📈time plot](bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa-vs-base-mem.svg)
- [📄table](bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa-vs-base.md)
- [📈time plot](bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa-vs-base.svg)

