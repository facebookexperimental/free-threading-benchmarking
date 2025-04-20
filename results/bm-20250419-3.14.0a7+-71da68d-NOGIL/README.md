# Results

- fork: python/71da68d5887b6c058907
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [71da68d](https://github.com/python/cpython/commit/71da68d)
- commit date: 2025-04-19T18:11:21Z
- commit merge base: [e7c5f60efc149dda3d3592fa2001f4583b128512](https://github.com/python/cpython/commit/e7c5f60efc149dda3d3592fa2001f4583b128512)
- commit date: 2025-04-19T18:11:21+00:00
- ref: 71da68d5887b6c058907

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14554120777)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250419-linux-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d.json)

### vs. 3.12.6

- Geometric mean: 1.138x faster (HPT: reliability of 99.75%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250419-linux-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.md)
- [📈time plot](bm-20250419-linux-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.097x faster (HPT: reliability of 99.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250419-linux-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250419-linux-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250419-linux-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base-mem.svg)
- [📄table](bm-20250419-linux-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.md)
- [📈time plot](bm-20250419-linux-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14554120777)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d.json)

### vs. 3.12.6

- Geometric mean: 1.027x faster (HPT: reliability of 64.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.md)
- [📈time plot](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 85.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base-mem.svg)
- [📄table](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.md)
- [📈time plot](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14554120777)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d.json)

### vs. 3.12.6

- Geometric mean: 1.113x faster (HPT: reliability of 99.79%, 1.01x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.md)
- [📈time plot](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 55.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.018x faster (HPT: reliability of 54.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base-mem.svg)
- [📄table](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.md)
- [📈time plot](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.svg)

