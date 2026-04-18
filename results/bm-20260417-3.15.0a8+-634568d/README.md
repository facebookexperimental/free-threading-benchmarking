# Results

- fork: python/634568d030f18183212c
- version: 3.15.0a8+
- config: 
- commit hash: [634568d](https://github.com/python/cpython/commit/634568d)
- commit date: 2026-04-17T17:21:13-07:00
- commit merge base: [db3e990b98fd12fee1bf851f4185d4e857318d76](https://github.com/python/cpython/commit/db3e990b98fd12fee1bf851f4185d4e857318d76)
- ref: 634568d030f18183212c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24592831132)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260417-vultr-x86_64-python-634568d030f18183212c-3.15.0a8%2B-634568d.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260417-vultr-x86_64-python-634568d030f18183212c-3.15.0a8%2B-634568d-vs-3.12.6.md)
- [📈time plot](bm-20260417-vultr-x86_64-python-634568d030f18183212c-3.15.0a8%2B-634568d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260417-vultr-x86_64-python-634568d030f18183212c-3.15.0a8%2B-634568d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260417-vultr-x86_64-python-634568d030f18183212c-3.15.0a8%2B-634568d-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24592831132)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260417-macm4pro-arm64-python-634568d030f18183212c-3.15.0a8%2B-634568d.json)

### vs. 3.12.6

- Geometric mean: 1.147x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260417-macm4pro-arm64-python-634568d030f18183212c-3.15.0a8%2B-634568d-vs-3.12.6.md)
- [📈time plot](bm-20260417-macm4pro-arm64-python-634568d030f18183212c-3.15.0a8%2B-634568d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x faster (HPT: reliability of 99.93%, 1.01x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260417-macm4pro-arm64-python-634568d030f18183212c-3.15.0a8%2B-634568d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260417-macm4pro-arm64-python-634568d030f18183212c-3.15.0a8%2B-634568d-vs-3.13.0rc2.svg)

