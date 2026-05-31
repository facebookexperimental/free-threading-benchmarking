# Results

- fork: python/1c7011d8feb8fa9a6877
- version: 3.16.0a0
- config: 
- commit hash: [1c7011d](https://github.com/python/cpython/commit/1c7011d)
- commit date: 2026-05-30T00:23:32+03:00
- commit merge base: [bcd29e466f55d8b4e3849ed6ada8ce86a46f5072](https://github.com/python/cpython/commit/bcd29e466f55d8b4e3849ed6ada8ce86a46f5072)
- ref: 1c7011d8feb8fa9a6877

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26669989012)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260530-vultr-x86_64-python-1c7011d8feb8fa9a6877-3.16.0a0-1c7011d.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260530-vultr-x86_64-python-1c7011d8feb8fa9a6877-3.16.0a0-1c7011d-vs-3.12.6.md)
- [📈time plot](bm-20260530-vultr-x86_64-python-1c7011d8feb8fa9a6877-3.16.0a0-1c7011d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 99.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260530-vultr-x86_64-python-1c7011d8feb8fa9a6877-3.16.0a0-1c7011d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260530-vultr-x86_64-python-1c7011d8feb8fa9a6877-3.16.0a0-1c7011d-vs-3.13.0rc2.svg)

