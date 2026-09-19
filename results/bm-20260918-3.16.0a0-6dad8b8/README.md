# Results

- fork: python/6dad8b88cc39d8f9f41c
- version: 3.16.0a0
- config: 
- commit hash: [6dad8b8](https://github.com/python/cpython/commit/6dad8b8)
- commit date: 2026-09-18T17:04:21-04:00
- commit merge base: [0e1ae61f7115db4c91dccc5fd9d7b8c801ef0b59](https://github.com/python/cpython/commit/0e1ae61f7115db4c91dccc5fd9d7b8c801ef0b59)
- ref: 6dad8b88cc39d8f9f41c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35410121133)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json)

### vs. 3.12.6

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8-vs-3.12.6.md)
- [📈time plot](bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 99.93%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8-vs-3.13.0rc2.md)
- [📈time plot](bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35410121133)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json)

### vs. 3.12.6

- Geometric mean: 1.143x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8-vs-3.12.6.md)
- [📈time plot](bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 99.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8-vs-3.13.0rc2.md)
- [📈time plot](bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8-vs-3.13.0rc2.svg)

