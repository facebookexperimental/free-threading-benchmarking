# Results

- fork: python/f1a47e79fb7081d3cde6
- version: 3.16.0a0
- config: NOGIL
- commit hash: [f1a47e7](https://github.com/python/cpython/commit/f1a47e7)
- commit date: 2026-05-14T01:21:03+02:00
- commit merge base: [50476a7e87926cf6a9ea978943c4a3d5d771c95f](https://github.com/python/cpython/commit/50476a7e87926cf6a9ea978943c4a3d5d771c95f)
- ref: f1a47e79fb7081d3cde6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25835285386)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7.json)

### vs. 3.12.6

- Geometric mean: 1.039x slower (HPT: reliability of 91.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.md)
- [📈time plot](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-base-mem.svg)
- [📄table](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-base.md)
- [📈time plot](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-base.svg)

