# Results

- fork: python/5197ecb5e4df30ba0f67
- version: 3.15.0a7+
- config: 
- commit hash: [5197ecb](https://github.com/python/cpython/commit/5197ecb)
- commit date: 2026-03-10T15:51:17-04:00
- commit merge base: [665c1db94f46f8e1a18a8c2f89adb3bc72cb83dc](https://github.com/python/cpython/commit/665c1db94f46f8e1a18a8c2f89adb3bc72cb83dc)
- ref: 5197ecb5e4df30ba0f67

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22930843267)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)
- [📈time plot](bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22930843267)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb.json)

### vs. 3.12.6

- Geometric mean: 1.134x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)
- [📈time plot](bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 98.31%, 1.00x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg)

