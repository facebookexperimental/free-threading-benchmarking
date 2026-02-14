# Results

- fork: python/fdbc135f9cf57599cca8
- version: 3.15.0a6+
- config: 
- commit hash: [fdbc135](https://github.com/python/cpython/commit/fdbc135)
- commit date: 2026-02-13T23:02:11Z
- commit merge base: [7359bb8dacc055bdcbb61f8fa4e375b25eedffd9](https://github.com/python/cpython/commit/7359bb8dacc055bdcbb61f8fa4e375b25eedffd9)
- commit date: 2026-02-13T23:02:11+00:00
- ref: fdbc135f9cf57599cca8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22007710721)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135-vs-3.12.6.md)
- [📈time plot](bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135-vs-3.13.0rc2.md)
- [📈time plot](bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22007710721)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135.json)

### vs. 3.12.6

- Geometric mean: 1.164x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135-vs-3.12.6.md)
- [📈time plot](bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135-vs-3.13.0rc2.md)
- [📈time plot](bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6%2B-fdbc135-vs-3.13.0rc2.svg)

