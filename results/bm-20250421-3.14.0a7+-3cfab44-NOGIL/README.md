# Results

- fork: python/3cfab449ab1e3c1472d2
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [3cfab44](https://github.com/python/cpython/commit/3cfab44)
- commit date: 2025-04-21T16:07:54-07:00
- commit merge base: [2b47f46d7dc30d27b2486991fea4acd83553294b](https://github.com/python/cpython/commit/2b47f46d7dc30d27b2486991fea4acd83553294b)
- ref: 3cfab449ab1e3c1472d2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14583977926)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250421-vultr-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44.json)

### vs. 3.12.6

- Geometric mean: 1.029x faster (HPT: reliability of 65.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250421-vultr-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.12.6.md)
- [📈time plot](bm-20250421-vultr-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 85.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250421-vultr-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.13.0rc2.md)
- [📈time plot](bm-20250421-vultr-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250421-vultr-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base-mem.svg)
- [📄table](bm-20250421-vultr-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base.md)
- [📈time plot](bm-20250421-vultr-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14583977926)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44.json)

### vs. 3.12.6

- Geometric mean: 1.111x faster (HPT: reliability of 99.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.12.6.md)
- [📈time plot](bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x faster (HPT: reliability of 57.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.13.0rc2.md)
- [📈time plot](bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x faster (HPT: reliability of 79.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base-mem.svg)
- [📄table](bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base.md)
- [📈time plot](bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base.svg)

