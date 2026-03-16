# Results

- fork: python/40095d526bd8ddbabee0
- version: 3.15.0a7+
- config: 
- commit hash: [40095d5](https://github.com/python/cpython/commit/40095d5)
- commit date: 2026-03-15T18:54:20-05:00
- commit merge base: [83edae33a5591c52fa45df38da2616af470f290a](https://github.com/python/cpython/commit/83edae33a5591c52fa45df38da2616af470f290a)
- ref: 40095d526bd8ddbabee0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23123222712)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.md)
- [📈time plot](bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23123222712)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5.json)

### vs. 3.12.6

- Geometric mean: 1.163x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.md)
- [📈time plot](bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.svg)

