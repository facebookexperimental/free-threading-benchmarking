# Results

- fork: python/f1a47e79fb7081d3cde6
- version: 3.16.0a0
- config: 
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

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.md)
- [📈time plot](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 99.07%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25835285386)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7.json)

### vs. 3.12.6

- Geometric mean: 1.158x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.md)
- [📈time plot](bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.svg)

