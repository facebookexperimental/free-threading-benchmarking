# Results

- fork: python/f41e9c750e6971c165e0
- version: 3.15.0a0
- config: NOGIL
- commit hash: [f41e9c7](https://github.com/python/cpython/commit/f41e9c7)
- commit date: 2025-07-01T13:26:13-04:00
- commit merge base: [86c3316183a79867e3c666d0830f897e16f0f339](https://github.com/python/cpython/commit/86c3316183a79867e3c666d0830f897e16f0f339)
- ref: f41e9c750e6971c165e0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16013149457)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 95.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.md)
- [📈time plot](bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 98.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base-mem.svg)
- [📄table](bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base.md)
- [📈time plot](bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16013149457)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 93.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.md)
- [📈time plot](bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 80.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x faster (HPT: reliability of 85.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base-mem.svg)
- [📄table](bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base.md)
- [📈time plot](bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base.svg)

