# Results

- fork: python/8865b4f95b32097099d2
- version: 3.15.0a0
- config: NOGIL
- commit hash: [8865b4f](https://github.com/python/cpython/commit/8865b4f)
- commit date: 2025-05-30T19:37:29+01:00
- commit merge base: [310c8cd5e5dcb0fb9509e08c0d5cf32075416878](https://github.com/python/cpython/commit/310c8cd5e5dcb0fb9509e08c0d5cf32075416878)
- ref: 8865b4f95b32097099d2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15358142265)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250530-vultr-x86_64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 88.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250530-vultr-x86_64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-3.12.6.md)
- [📈time plot](bm-20250530-vultr-x86_64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x slower (HPT: reliability of 95.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250530-vultr-x86_64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250530-vultr-x86_64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250530-vultr-x86_64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-base-mem.svg)
- [📄table](bm-20250530-vultr-x86_64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-base.md)
- [📈time plot](bm-20250530-vultr-x86_64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15358142265)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250530-macm4pro-arm64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 97.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250530-macm4pro-arm64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-3.12.6.md)
- [📈time plot](bm-20250530-macm4pro-arm64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 70.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250530-macm4pro-arm64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250530-macm4pro-arm64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.015x slower (HPT: reliability of 97.02%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250530-macm4pro-arm64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-base-mem.svg)
- [📄table](bm-20250530-macm4pro-arm64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-base.md)
- [📈time plot](bm-20250530-macm4pro-arm64-python-8865b4f95b32097099d2-3.15.0a0-8865b4f-vs-base.svg)

