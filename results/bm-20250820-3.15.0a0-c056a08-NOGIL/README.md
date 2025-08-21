# Results

- fork: python/c056a089d8573b03c62d
- version: 3.15.0a0
- config: NOGIL
- commit hash: [c056a08](https://github.com/python/cpython/commit/c056a08)
- commit date: 2025-08-20T22:59:40+01:00
- commit merge base: [7dc42b67a75f58a2b1c0a4560bd4bf8ff25cac8b](https://github.com/python/cpython/commit/7dc42b67a75f58a2b1c0a4560bd4bf8ff25cac8b)
- ref: c056a089d8573b03c62d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17113643634)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250820-vultr-x86_64-python-c056a089d8573b03c62d-3.15.0a0-c056a08.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 93.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250820-vultr-x86_64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-3.12.6.md)
- [📈time plot](bm-20250820-vultr-x86_64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 97.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250820-vultr-x86_64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-3.13.0rc2.md)
- [📈time plot](bm-20250820-vultr-x86_64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250820-vultr-x86_64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-base-mem.svg)
- [📄table](bm-20250820-vultr-x86_64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-base.md)
- [📈time plot](bm-20250820-vultr-x86_64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17113643634)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250820-macm4pro-arm64-python-c056a089d8573b03c62d-3.15.0a0-c056a08.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 90.31%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250820-macm4pro-arm64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-3.12.6.md)
- [📈time plot](bm-20250820-macm4pro-arm64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 88.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250820-macm4pro-arm64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-3.13.0rc2.md)
- [📈time plot](bm-20250820-macm4pro-arm64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 99.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250820-macm4pro-arm64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-base-mem.svg)
- [📄table](bm-20250820-macm4pro-arm64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-base.md)
- [📈time plot](bm-20250820-macm4pro-arm64-python-c056a089d8573b03c62d-3.15.0a0-c056a08-vs-base.svg)

