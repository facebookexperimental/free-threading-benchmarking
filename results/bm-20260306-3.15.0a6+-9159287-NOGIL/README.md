# Results

- fork: python/9159287f58f7a5a7e59e
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [9159287](https://github.com/python/cpython/commit/9159287)
- commit date: 2026-03-06T21:57:44Z
- commit merge base: [c1d77683213c400fca144692654845e6f5418981](https://github.com/python/cpython/commit/c1d77683213c400fca144692654845e6f5418981)
- commit date: 2026-03-06T21:57:44+00:00
- ref: 9159287f58f7a5a7e59e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22787841255)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260306-vultr-x86_64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 77.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260306-vultr-x86_64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-3.12.6.md)
- [📈time plot](bm-20260306-vultr-x86_64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 91.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260306-vultr-x86_64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-3.13.0rc2.md)
- [📈time plot](bm-20260306-vultr-x86_64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260306-vultr-x86_64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-base-mem.svg)
- [📄table](bm-20260306-vultr-x86_64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-base.md)
- [📈time plot](bm-20260306-vultr-x86_64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22787841255)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260306-macm4pro-arm64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 99.93%, 1.01x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260306-macm4pro-arm64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-3.12.6.md)
- [📈time plot](bm-20260306-macm4pro-arm64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 65.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260306-macm4pro-arm64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-3.13.0rc2.md)
- [📈time plot](bm-20260306-macm4pro-arm64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.038x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260306-macm4pro-arm64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-base-mem.svg)
- [📄table](bm-20260306-macm4pro-arm64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-base.md)
- [📈time plot](bm-20260306-macm4pro-arm64-python-9159287f58f7a5a7e59e-3.15.0a6%2B-9159287-vs-base.svg)

