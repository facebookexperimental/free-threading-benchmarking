# Results

- fork: python/c4bcc6a77864b42574ec
- version: 3.14.0a7+
- config: 
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

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.12.6.md)
- [📈time plot](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250506-vultr-x86_64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14849033548)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a.json)

### vs. 3.12.6

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.12.6.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 65.44%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7%2B-c4bcc6a-vs-3.13.0rc2.svg)

