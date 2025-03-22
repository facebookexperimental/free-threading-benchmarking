# Results

- fork: python/b70d45ab22e1d0f3b8a0
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [b70d45a](https://github.com/python/cpython/commit/b70d45a)
- commit date: 2025-03-21T11:12:35+01:00
- commit merge base: [e0fda794fadb09f08a5d1a04aa6a7e0b42a99666](https://github.com/python/cpython/commit/e0fda794fadb09f08a5d1a04aa6a7e0b42a99666)
- ref: b70d45ab22e1d0f3b8a0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14011150616)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 99.98%, 1.02x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a-vs-3.12.6.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14011153639)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a.json)

### vs. 3.12.6

- Geometric mean: 1.020x slower (HPT: reliability of 99.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a-vs-3.12.6.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.091x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6%2B-b70d45a-vs-3.13.0rc2.svg)

