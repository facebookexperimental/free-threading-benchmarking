# Results

- fork: python/012c498035a9adfe9fd2
- version: 3.15.0a5+
- config: JIT
- commit hash: [012c498](https://github.com/python/cpython/commit/012c498)
- commit date: 2026-01-24T11:13:50Z
- commit merge base: [5f736a0432c2e43de8f35d9a75aa814e4407e637](https://github.com/python/cpython/commit/5f736a0432c2e43de8f35d9a75aa814e4407e637)
- commit date: 2026-01-24T11:13:50+00:00
- ref: 012c498035a9adfe9fd2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21315070429)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498.json)

### vs. 3.12.6

- Geometric mean: 1.139x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498-vs-3.12.6.md)
- [📈time plot](bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498-vs-3.13.0rc2.md)
- [📈time plot](bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21315070429)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498.json)

### vs. 3.12.6

- Geometric mean: 1.254x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498-vs-3.12.6.md)
- [📈time plot](bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.164x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498-vs-3.13.0rc2.md)
- [📈time plot](bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5%2B-012c498-vs-3.13.0rc2.svg)

