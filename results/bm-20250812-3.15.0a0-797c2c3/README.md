# Results

- fork: python/797c2c33e181badc053f
- version: 3.15.0a0
- config: 
- commit hash: [797c2c3](https://github.com/python/cpython/commit/797c2c3)
- commit date: 2025-08-12T23:28:38+01:00
- commit merge base: [e93dca72232efe6d5cf2d52ea6dd3967ff61360b](https://github.com/python/cpython/commit/e93dca72232efe6d5cf2d52ea6dd3967ff61360b)
- ref: 797c2c33e181badc053f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16924207826)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250812-vultr-x86_64-python-797c2c33e181badc053f-3.15.0a0-797c2c3.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250812-vultr-x86_64-python-797c2c33e181badc053f-3.15.0a0-797c2c3-vs-3.12.6.md)
- [📈time plot](bm-20250812-vultr-x86_64-python-797c2c33e181badc053f-3.15.0a0-797c2c3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250812-vultr-x86_64-python-797c2c33e181badc053f-3.15.0a0-797c2c3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250812-vultr-x86_64-python-797c2c33e181badc053f-3.15.0a0-797c2c3-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16924207826)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3-vs-3.12.6.md)
- [📈time plot](bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 55.02%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3-vs-3.13.0rc2.svg)

