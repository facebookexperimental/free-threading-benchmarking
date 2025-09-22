# Results

- fork: python/9c3d09b984374292d1d8
- version: 3.15.0a0
- config: 
- commit hash: [9c3d09b](https://github.com/python/cpython/commit/9c3d09b)
- commit date: 2025-09-21T14:57:13-04:00
- commit merge base: [cb6fed0d7e3f5104b76ef2febc51f11a94aa2e04](https://github.com/python/cpython/commit/cb6fed0d7e3f5104b76ef2febc51f11a94aa2e04)
- ref: 9c3d09b984374292d1d8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17901073158)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250921-vultr-x86_64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250921-vultr-x86_64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b-vs-3.12.6.md)
- [📈time plot](bm-20250921-vultr-x86_64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250921-vultr-x86_64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250921-vultr-x86_64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17901073158)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250921-macm4pro-arm64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b.json)

### vs. 3.12.6

- Geometric mean: 1.131x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250921-macm4pro-arm64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b-vs-3.12.6.md)
- [📈time plot](bm-20250921-macm4pro-arm64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250921-macm4pro-arm64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250921-macm4pro-arm64-python-9c3d09b984374292d1d8-3.15.0a0-9c3d09b-vs-3.13.0rc2.svg)

