# Results

- fork: python/3db3bba4d1feb3a9fbfc
- version: 3.16.0a0
- config: NOGIL
- commit hash: [3db3bba](https://github.com/python/cpython/commit/3db3bba)
- commit date: 2026-06-24T23:30:51+00:00
- commit merge base: [b41dc4ac6354dd563258a9766325496c3b2e82e1](https://github.com/python/cpython/commit/b41dc4ac6354dd563258a9766325496c3b2e82e1)
- ref: 3db3bba4d1feb3a9fbfc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28139790006)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 84.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba-vs-3.12.6.md)
- [📈time plot](bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 97.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba-vs-3.13.0rc2.md)
- [📈time plot](bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.17x
- [🧠memory plot](bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba-vs-base-mem.svg)
- [📄table](bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba-vs-base.md)
- [📈time plot](bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba-vs-base.svg)

