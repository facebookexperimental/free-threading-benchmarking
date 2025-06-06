# Results

- fork: python/71da68d5887b6c058907
- version: 3.14.0a7+
- config: CLANG
- commit hash: [71da68d](https://github.com/python/cpython/commit/71da68d)
- commit date: 2025-04-19T18:11:21Z
- commit merge base: [e7c5f60efc149dda3d3592fa2001f4583b128512](https://github.com/python/cpython/commit/e7c5f60efc149dda3d3592fa2001f4583b128512)
- commit date: 2025-04-19T18:11:21+00:00
- ref: 71da68d5887b6c058907

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14554120777)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d.json)

### vs. 3.12.6

- Geometric mean: 1.175x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.md)
- [📈time plot](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.134x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.053x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base-mem.svg)
- [📄table](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.md)
- [📈time plot](bm-20250419-vultr-x86_64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14554120777)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d.json)

### vs. 3.12.6

- Geometric mean: 1.157x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.md)
- [📈time plot](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base-mem.svg)
- [📄table](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.md)
- [📈time plot](bm-20250419-macm4pro-arm64-python-71da68d5887b6c058907-3.14.0a7%2B-71da68d-vs-base.svg)

