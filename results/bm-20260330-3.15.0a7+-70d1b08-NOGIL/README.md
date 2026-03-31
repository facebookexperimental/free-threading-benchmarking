# Results

- fork: python/70d1b08a4bb52652094c
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [70d1b08](https://github.com/python/cpython/commit/70d1b08)
- commit date: 2026-03-30T20:31:36Z
- commit merge base: [ca95e979d6c9c62696bf3c162ddc21eae841c804](https://github.com/python/cpython/commit/ca95e979d6c9c62696bf3c162ddc21eae841c804)
- commit date: 2026-03-30T20:31:36+00:00
- ref: 70d1b08a4bb52652094c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23774846607)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 58.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.md)
- [📈time plot](bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 78.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.md)
- [📈time plot](bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base-mem.svg)
- [📄table](bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base.md)
- [📈time plot](bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23774846607)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 99.45%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.md)
- [📈time plot](bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.015x faster (HPT: reliability of 52.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.md)
- [📈time plot](bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.054x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base-mem.svg)
- [📄table](bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base.md)
- [📈time plot](bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base.svg)

