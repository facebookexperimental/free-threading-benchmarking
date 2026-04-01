# Results

- fork: python/9e1f1644cd7b7661f074
- version: 3.15.0a7+
- config: 
- commit hash: [9e1f164](https://github.com/python/cpython/commit/9e1f164)
- commit date: 2026-03-31T17:52:11-04:00
- commit merge base: [62a6e898e017c9878490544f6a227b8a187a949c](https://github.com/python/cpython/commit/62a6e898e017c9878490544f6a227b8a187a949c)
- ref: 9e1f1644cd7b7661f074

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23826382346)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.md)
- [📈time plot](bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.md)
- [📈time plot](bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23826382346)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164.json)

### vs. 3.12.6

- Geometric mean: 1.162x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.md)
- [📈time plot](bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.md)
- [📈time plot](bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.svg)

