# Results

- fork: python/6ea3f8cd7ff4ff9769ae
- version: 3.15.0a5+
- config: 
- commit hash: [6ea3f8c](https://github.com/python/cpython/commit/6ea3f8c)
- commit date: 2026-01-27T17:52:50-05:00
- commit merge base: [6b4538192ddac518b9c15b3f79445c964330dee3](https://github.com/python/cpython/commit/6b4538192ddac518b9c15b3f79445c964330dee3)
- ref: 6ea3f8cd7ff4ff9769ae

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21419884118)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.md)
- [📈time plot](bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.041x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21419884118)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c.json)

### vs. 3.12.6

- Geometric mean: 1.185x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.md)
- [📈time plot](bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.svg)

