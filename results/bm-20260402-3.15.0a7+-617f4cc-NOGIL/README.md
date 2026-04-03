# Results

- fork: python/617f4cc1c2605b86b483
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [617f4cc](https://github.com/python/cpython/commit/617f4cc)
- commit date: 2026-04-02T23:26:21+02:00
- commit merge base: [c1b20a6d96eadf1c49c511f1e480aff82b6477a4](https://github.com/python/cpython/commit/c1b20a6d96eadf1c49c511f1e480aff82b6477a4)
- ref: 617f4cc1c2605b86b483

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23928626687)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260402-vultr-x86_64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 85.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260402-vultr-x86_64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-3.12.6.md)
- [📈time plot](bm-20260402-vultr-x86_64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 94.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260402-vultr-x86_64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-3.13.0rc2.md)
- [📈time plot](bm-20260402-vultr-x86_64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260402-vultr-x86_64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-base-mem.svg)
- [📄table](bm-20260402-vultr-x86_64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-base.md)
- [📈time plot](bm-20260402-vultr-x86_64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23928626687)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260402-macm4pro-arm64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 99.62%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260402-macm4pro-arm64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-3.12.6.md)
- [📈time plot](bm-20260402-macm4pro-arm64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 52.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260402-macm4pro-arm64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-3.13.0rc2.md)
- [📈time plot](bm-20260402-macm4pro-arm64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.049x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260402-macm4pro-arm64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-base-mem.svg)
- [📄table](bm-20260402-macm4pro-arm64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-base.md)
- [📈time plot](bm-20260402-macm4pro-arm64-python-617f4cc1c2605b86b483-3.15.0a7%2B-617f4cc-vs-base.svg)

