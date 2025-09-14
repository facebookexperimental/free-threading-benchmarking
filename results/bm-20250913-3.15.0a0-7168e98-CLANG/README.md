# Results

- fork: python/7168e98c80d28ab71f39
- version: 3.15.0a0
- config: CLANG
- commit hash: [7168e98](https://github.com/python/cpython/commit/7168e98)
- commit date: 2025-09-13T19:27:04+02:00
- commit merge base: [430900d15b3d3abb5c6460fbdbf90f4d6561397d](https://github.com/python/cpython/commit/430900d15b3d3abb5c6460fbdbf90f4d6561397d)
- ref: 7168e98c80d28ab71f39

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17703822657)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98.json)

### vs. 3.12.6

- Geometric mean: 1.123x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.12.6.md)
- [📈time plot](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.13.0rc2.md)
- [📈time plot](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-base-mem.svg)
- [📄table](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-base.md)
- [📈time plot](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17703822657)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98.json)

### vs. 3.12.6

- Geometric mean: 1.139x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.12.6.md)
- [📈time plot](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.13.0rc2.md)
- [📈time plot](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.034x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-base-mem.svg)
- [📄table](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-base.md)
- [📈time plot](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-base.svg)

