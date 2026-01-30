# Results

- fork: python/5f57f6970bdea45cc2b1
- version: 3.15.0a5+
- config: 
- commit hash: [5f57f69](https://github.com/python/cpython/commit/5f57f69)
- commit date: 2026-01-30T00:35:30Z
- commit merge base: [1b081434666d244d2fa083d47251d90175ac69da](https://github.com/python/cpython/commit/1b081434666d244d2fa083d47251d90175ac69da)
- commit date: 2026-01-30T00:35:30+00:00
- ref: 5f57f6970bdea45cc2b1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21499965912)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.md)
- [📈time plot](bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.md)
- [📈time plot](bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21499965912)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69.json)

### vs. 3.12.6

- Geometric mean: 1.200x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.md)
- [📈time plot](bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.113x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.md)
- [📈time plot](bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.svg)

