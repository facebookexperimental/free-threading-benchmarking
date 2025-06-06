# Results

- fork: python/6d5a8c2ec19f1c38b455
- version: 3.15.0a0
- config: NOGIL
- commit hash: [6d5a8c2](https://github.com/python/cpython/commit/6d5a8c2)
- commit date: 2025-05-09T08:17:50+08:00
- commit merge base: [c492ac72525ea5887082ee991b45cc237cd02a40](https://github.com/python/cpython/commit/c492ac72525ea5887082ee991b45cc237cd02a40)
- ref: 6d5a8c2ec19f1c38b455

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14918738192)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250509-vultr-x86_64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2.json)

### vs. 3.12.6

- Geometric mean: 1.010x faster (HPT: reliability of 91.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250509-vultr-x86_64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-3.12.6.md)
- [📈time plot](bm-20250509-vultr-x86_64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x slower (HPT: reliability of 97.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250509-vultr-x86_64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-3.13.0rc2.md)
- [📈time plot](bm-20250509-vultr-x86_64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.23x
- [🧠memory plot](bm-20250509-vultr-x86_64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-base-mem.svg)
- [📄table](bm-20250509-vultr-x86_64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-base.md)
- [📈time plot](bm-20250509-vultr-x86_64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14918738192)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 96.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-3.12.6.md)
- [📈time plot](bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x faster (HPT: reliability of 70.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-3.13.0rc2.md)
- [📈time plot](bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.021x slower (HPT: reliability of 99.01%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-base-mem.svg)
- [📄table](bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-base.md)
- [📈time plot](bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2-vs-base.svg)

