# Results

- fork: python/d687900f98114bb5910d
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [d687900](https://github.com/python/cpython/commit/d687900)
- commit date: 2025-04-09T16:18:54-07:00
- commit merge base: [e5237541a098e32a70fc621dee08721a72be7eb8](https://github.com/python/cpython/commit/e5237541a098e32a70fc621dee08721a72be7eb8)
- ref: d687900f98114bb5910d

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14369543971)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250409-linux-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900.json)

### vs. 3.12.6

- Geometric mean: 1.038x faster (HPT: reliability of 69.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250409-linux-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.12.6.md)
- [📈time plot](bm-20250409-linux-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x slower (HPT: reliability of 76.37%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250409-linux-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.13.0rc2.md)
- [📈time plot](bm-20250409-linux-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250409-linux-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base-mem.svg)
- [📄table](bm-20250409-linux-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base.md)
- [📈time plot](bm-20250409-linux-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14369543971)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250409-vultr-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900.json)

### vs. 3.12.6

- Geometric mean: 1.016x slower (HPT: reliability of 99.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250409-vultr-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.12.6.md)
- [📈time plot](bm-20250409-vultr-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x slower (HPT: reliability of 99.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250409-vultr-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.13.0rc2.md)
- [📈time plot](bm-20250409-vultr-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.125x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250409-vultr-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base-mem.svg)
- [📄table](bm-20250409-vultr-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base.md)
- [📈time plot](bm-20250409-vultr-x86_64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14369543971)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250409-macm4pro-arm64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900.json)

### vs. 3.12.6

- Geometric mean: 1.103x faster (HPT: reliability of 98.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250409-macm4pro-arm64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.12.6.md)
- [📈time plot](bm-20250409-macm4pro-arm64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 59.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250409-macm4pro-arm64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.13.0rc2.md)
- [📈time plot](bm-20250409-macm4pro-arm64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 97.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250409-macm4pro-arm64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base-mem.svg)
- [📄table](bm-20250409-macm4pro-arm64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base.md)
- [📈time plot](bm-20250409-macm4pro-arm64-python-d687900f98114bb5910d-3.14.0a7%2B-d687900-vs-base.svg)

