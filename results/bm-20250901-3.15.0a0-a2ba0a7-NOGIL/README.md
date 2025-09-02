# Results

- fork: python/a2ba0a7552580f616f74
- version: 3.15.0a0
- config: NOGIL
- commit hash: [a2ba0a7](https://github.com/python/cpython/commit/a2ba0a7)
- commit date: 2025-09-01T17:14:23-07:00
- commit merge base: [47bc10e6b3cb44658da275f3484781ef2a2b9222](https://github.com/python/cpython/commit/47bc10e6b3cb44658da275f3484781ef2a2b9222)
- ref: a2ba0a7552580f616f74

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17389755429)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 84.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.md)
- [📈time plot](bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 96.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base-mem.svg)
- [📄table](bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base.md)
- [📈time plot](bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17389755429)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 92.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.md)
- [📈time plot](bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x slower (HPT: reliability of 81.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.024x slower (HPT: reliability of 99.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base-mem.svg)
- [📄table](bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base.md)
- [📈time plot](bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base.svg)

