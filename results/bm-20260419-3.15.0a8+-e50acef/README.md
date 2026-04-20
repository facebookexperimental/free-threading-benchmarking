# Results

- fork: python/e50acef0b2c2057874a9
- version: 3.15.0a8+
- config: 
- commit hash: [e50acef](https://github.com/python/cpython/commit/e50acef)
- commit date: 2026-04-19T17:05:50-07:00
- commit merge base: [82767780f8de2fc492567ceb6a590101ae3b19ad](https://github.com/python/cpython/commit/82767780f8de2fc492567ceb6a590101ae3b19ad)
- ref: e50acef0b2c2057874a9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24643337844)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.md)
- [📈time plot](bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.md)
- [📈time plot](bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24643337844)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef.json)

### vs. 3.12.6

- Geometric mean: 1.162x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.md)
- [📈time plot](bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.md)
- [📈time plot](bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.svg)

