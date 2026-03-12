# Results

- fork: python/d19de375a204c74ab5f3
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [d19de37](https://github.com/python/cpython/commit/d19de37)
- commit date: 2026-03-11T21:08:18Z
- commit merge base: [f062014d3876f1f81c0e60bf861c3460429ac3b4](https://github.com/python/cpython/commit/f062014d3876f1f81c0e60bf861c3460429ac3b4)
- commit date: 2026-03-11T21:08:18+00:00
- ref: d19de375a204c74ab5f3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22981095445)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 72.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)
- [📈time plot](bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 87.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)
- [📈time plot](bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base-mem.svg)
- [📄table](bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.md)
- [📈time plot](bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22981095445)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37.json)

### vs. 3.12.6

- Geometric mean: 1.105x faster (HPT: reliability of 99.74%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: asyncio_websockets, chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)
- [📈time plot](bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 50.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: asyncio_websockets, chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)
- [📈time plot](bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.057x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 asyncio_websockets
- [🧠memory plot](bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base-mem.svg)
- [📄table](bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.md)
- [📈time plot](bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.svg)

