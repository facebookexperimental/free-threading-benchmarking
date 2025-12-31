# Results

- fork: python/04899b8539ab83657a44
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [04899b8](https://github.com/python/cpython/commit/04899b8)
- commit date: 2025-12-30T15:24:32-08:00
- commit merge base: [aa8a43d179bad5cd9fbfce63b630e2ee0bd617e4](https://github.com/python/cpython/commit/aa8a43d179bad5cd9fbfce63b630e2ee0bd617e4)
- ref: 04899b8539ab83657a44

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20609021695)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 83.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.12.6.md)
- [📈time plot](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 93.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-base-mem.svg)
- [📄table](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-base.md)
- [📈time plot](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20609021695)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 98.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.12.6.md)
- [📈time plot](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 62.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.060x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-base-mem.svg)
- [📄table](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-base.md)
- [📈time plot](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-base.svg)

