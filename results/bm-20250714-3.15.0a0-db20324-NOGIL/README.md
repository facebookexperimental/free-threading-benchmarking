# Results

- fork: python/db2032407a0c4928f3bd
- version: 3.15.0a0
- config: NOGIL
- commit hash: [db20324](https://github.com/python/cpython/commit/db20324)
- commit date: 2025-07-14T17:01:56-07:00
- commit merge base: [9363703bd3bf86e363c14a02e3d729caf1e29f44](https://github.com/python/cpython/commit/9363703bd3bf86e363c14a02e3d729caf1e29f44)
- ref: db2032407a0c4928f3bd

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16281010016)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250714-vultr-x86_64-python-db2032407a0c4928f3bd-3.15.0a0-db20324.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 95.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250714-vultr-x86_64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-3.12.6.md)
- [📈time plot](bm-20250714-vultr-x86_64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 95.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250714-vultr-x86_64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-3.13.0rc2.md)
- [📈time plot](bm-20250714-vultr-x86_64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250714-vultr-x86_64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-base-mem.svg)
- [📄table](bm-20250714-vultr-x86_64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-base.md)
- [📈time plot](bm-20250714-vultr-x86_64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16281010016)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250714-macm4pro-arm64-python-db2032407a0c4928f3bd-3.15.0a0-db20324.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 98.55%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250714-macm4pro-arm64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-3.12.6.md)
- [📈time plot](bm-20250714-macm4pro-arm64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 68.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250714-macm4pro-arm64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-3.13.0rc2.md)
- [📈time plot](bm-20250714-macm4pro-arm64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 98.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250714-macm4pro-arm64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-base-mem.svg)
- [📄table](bm-20250714-macm4pro-arm64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-base.md)
- [📈time plot](bm-20250714-macm4pro-arm64-python-db2032407a0c4928f3bd-3.15.0a0-db20324-vs-base.svg)

