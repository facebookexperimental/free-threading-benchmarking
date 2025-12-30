# Results

- fork: python/b6b0e14b3d4aa9e9b89b
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [b6b0e14](https://github.com/python/cpython/commit/b6b0e14)
- commit date: 2025-12-29T18:30:51+01:00
- commit merge base: [6cb245d26086369bb075858501405865fc255a10](https://github.com/python/cpython/commit/6cb245d26086369bb075858501405865fc255a10)
- ref: b6b0e14b3d4aa9e9b89b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20585822892)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 86.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-3.12.6.md)
- [📈time plot](bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 95.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-3.13.0rc2.md)
- [📈time plot](bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-base-mem.svg)
- [📄table](bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-base.md)
- [📈time plot](bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20585822892)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 94.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-3.12.6.md)
- [📈time plot](bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 81.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-3.13.0rc2.md)
- [📈time plot](bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.064x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 asyncio_websockets
- [🧠memory plot](bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-base-mem.svg)
- [📄table](bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-base.md)
- [📈time plot](bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3%2B-b6b0e14-vs-base.svg)

