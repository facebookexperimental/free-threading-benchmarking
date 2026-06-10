# Results

- fork: python/29a920e80e21490b5bdb
- version: 3.16.0a0
- config: 
- commit hash: [29a920e](https://github.com/python/cpython/commit/29a920e)
- commit date: 2026-06-08T22:38:14+03:00
- commit merge base: [fccf67a35449920484ea11d8a16566b58b0c4519](https://github.com/python/cpython/commit/fccf67a35449920484ea11d8a16566b58b0c4519)
- ref: 29a920e80e21490b5bdb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27176962709)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260608-vultr-x86_64-python-29a920e80e21490b5bdb-3.16.0a0-29a920e.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260608-vultr-x86_64-python-29a920e80e21490b5bdb-3.16.0a0-29a920e-vs-3.12.6.md)
- [📈time plot](bm-20260608-vultr-x86_64-python-29a920e80e21490b5bdb-3.16.0a0-29a920e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 99.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260608-vultr-x86_64-python-29a920e80e21490b5bdb-3.16.0a0-29a920e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260608-vultr-x86_64-python-29a920e80e21490b5bdb-3.16.0a0-29a920e-vs-3.13.0rc2.svg)

