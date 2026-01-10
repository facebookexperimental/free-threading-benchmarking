# Results

- fork: python/95259116ecb4346b570b
- version: 3.15.0a3+
- config: 
- commit hash: [9525911](https://github.com/python/cpython/commit/9525911)
- commit date: 2026-01-09T23:18:22Z
- commit merge base: [e0fb278064932a0a9faf5d06850a0d211c57dfc9](https://github.com/python/cpython/commit/e0fb278064932a0a9faf5d06850a0d211c57dfc9)
- commit date: 2026-01-09T23:18:22+00:00
- ref: 95259116ecb4346b570b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20869636657)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911-vs-3.12.6.md)
- [📈time plot](bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911-vs-3.13.0rc2.md)
- [📈time plot](bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20869636657)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911.json)

### vs. 3.12.6

- Geometric mean: 1.161x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911-vs-3.12.6.md)
- [📈time plot](bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911-vs-3.13.0rc2.md)
- [📈time plot](bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3%2B-9525911-vs-3.13.0rc2.svg)

