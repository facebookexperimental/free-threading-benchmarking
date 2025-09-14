# Results

- fork: python/7168e98c80d28ab71f39
- version: 3.15.0a0
- config: 
- commit hash: [7168e98](https://github.com/python/cpython/commit/7168e98)
- commit date: 2025-09-13T19:27:04+02:00
- commit merge base: [430900d15b3d3abb5c6460fbdbf90f4d6561397d](https://github.com/python/cpython/commit/430900d15b3d3abb5c6460fbdbf90f4d6561397d)
- ref: 7168e98c80d28ab71f39

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17703822657)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-pystats.json)
- [pystats table](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-pystats.md)
- [raw results](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.12.6.md)
- [📈time plot](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.13.0rc2.md)
- [📈time plot](bm-20250913-vultr-x86_64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17703822657)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.12.6.md)
- [📈time plot](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 87.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.13.0rc2.md)
- [📈time plot](bm-20250913-macm4pro-arm64-python-7168e98c80d28ab71f39-3.15.0a0-7168e98-vs-3.13.0rc2.svg)

