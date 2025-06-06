# Results

- fork: python/c4bcc6a77864b42574ec
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [c4bcc6a](https://github.com/python/cpython/commit/c4bcc6a)
- commit date: 2025-05-06T01:03:55+01:00
- commit merge base: [e6f8e0a035f4cbeffb331d90c295ab5894852c39](https://github.com/python/cpython/commit/e6f8e0a035f4cbeffb331d90c295ab5894852c39)
- ref: c4bcc6a77864b42574ec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14849033548)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a.json)

### vs. 3.12.6

- Geometric mean: 1.002x slower (HPT: reliability of 95.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.12.6.md)
- [📈time plot](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x slower (HPT: reliability of 96.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- new benchmarks: coverage, html5lib, sqlalchemy_declarative, sqlalchemy_imperative
- [🧠memory plot](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-base-mem.svg)
- [📄table](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-base.md)
- [📈time plot](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14849033548)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 98.01%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.12.6.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x faster (HPT: reliability of 65.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 97.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-base-mem.svg)
- [📄table](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-base.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-base.svg)

