# Results

- fork: python/04899b8539ab83657a44
- version: 3.15.0a3+
- config: 
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

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.12.6.md)
- [📈time plot](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251230-vultr-x86_64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20609021695)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8.json)

### vs. 3.12.6

- Geometric mean: 1.160x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.12.6.md)
- [📈time plot](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251230-macm4pro-arm64-python-04899b8539ab83657a44-3.15.0a3%2B-04899b8-vs-3.13.0rc2.svg)

