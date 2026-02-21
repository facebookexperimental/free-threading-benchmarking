# Results

- fork: python/06292614ff7cef0ba28d
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [0629261](https://github.com/python/cpython/commit/0629261)
- commit date: 2026-02-20T19:25:45-05:00
- commit merge base: [70da972f97ec799dc7d7ab069fe195455f2f81b2](https://github.com/python/cpython/commit/70da972f97ec799dc7d7ab069fe195455f2f81b2)
- ref: 06292614ff7cef0ba28d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22246659723)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260220-vultr-x86_64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 70.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260220-vultr-x86_64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-3.12.6.md)
- [📈time plot](bm-20260220-vultr-x86_64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 86.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260220-vultr-x86_64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-3.13.0rc2.md)
- [📈time plot](bm-20260220-vultr-x86_64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20260220-vultr-x86_64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-base-mem.svg)
- [📄table](bm-20260220-vultr-x86_64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-base.md)
- [📈time plot](bm-20260220-vultr-x86_64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22246659723)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261.json)

### vs. 3.12.6

- Geometric mean: 1.098x faster (HPT: reliability of 99.88%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-3.12.6.md)
- [📈time plot](bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 58.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-3.13.0rc2.md)
- [📈time plot](bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.032x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-base-mem.svg)
- [📄table](bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-base.md)
- [📈time plot](bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6%2B-0629261-vs-base.svg)

