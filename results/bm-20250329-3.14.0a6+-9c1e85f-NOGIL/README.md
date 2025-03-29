# Results

- fork: python/9c1e85fd64cf6a85f7c9
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [9c1e85f](https://github.com/python/cpython/commit/9c1e85f)
- commit date: 2025-03-29T08:58:17+09:00
- commit merge base: [2984ff9e5196aa575c7322c2040d55dd4d4eaa02](https://github.com/python/cpython/commit/2984ff9e5196aa575c7322c2040d55dd4d4eaa02)
- ref: 9c1e85fd64cf6a85f7c9

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14140210577)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250329-linux-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f.json)

### vs. 3.12.6

- Geometric mean: 1.037x faster (HPT: reliability of 80.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250329-linux-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.12.6.md)
- [📈time plot](bm-20250329-linux-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x slower (HPT: reliability of 91.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250329-linux-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250329-linux-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.116x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250329-linux-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base-mem.svg)
- [📄table](bm-20250329-linux-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base.md)
- [📈time plot](bm-20250329-linux-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14140210577)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250329-vultr-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f.json)

### vs. 3.12.6

- Geometric mean: 1.083x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250329-vultr-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.12.6.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.113x slower (HPT: reliability of 99.99%, 1.08x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250329-vultr-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.175x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250329-vultr-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base-mem.svg)
- [📄table](bm-20250329-vultr-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14140210577)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 97.03%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.12.6.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 65.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.041x faster (HPT: reliability of 99.86%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base-mem.svg)
- [📄table](bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6%2B-9c1e85f-vs-base.svg)

