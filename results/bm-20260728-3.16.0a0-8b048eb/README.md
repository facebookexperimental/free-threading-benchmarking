# Results

- fork: python/8b048eb35eb7f83dbff8
- version: 3.16.0a0
- config: 
- commit hash: [8b048eb](https://github.com/python/cpython/commit/8b048eb)
- commit date: 2026-07-28T20:35:26+03:00
- commit merge base: [e3634bb44f7f1395dcb1b7ab3736811e9e2a4589](https://github.com/python/cpython/commit/e3634bb44f7f1395dcb1b7ab3736811e9e2a4589)
- ref: 8b048eb35eb7f83dbff8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30411823826)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json)

### vs. 3.12.6

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb-vs-3.12.6.md)
- [📈time plot](bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 99.38%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb-vs-3.13.0rc2.svg)

