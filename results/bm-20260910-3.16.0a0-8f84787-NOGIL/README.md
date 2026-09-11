# Results

- fork: python/8f847875d60c81841e18
- version: 3.16.0a0
- config: NOGIL
- commit hash: [8f84787](https://github.com/python/cpython/commit/8f84787)
- commit date: 2026-09-10T22:21:15+01:00
- commit merge base: [bba99f2b3272cbe47af9bee05a294961c0528829](https://github.com/python/cpython/commit/bba99f2b3272cbe47af9bee05a294961c0528829)
- ref: 8f847875d60c81841e18

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34547459887)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787.json)

### vs. 3.12.6

- Geometric mean: 1.052x slower (HPT: reliability of 91.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.md)
- [📈time plot](bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x slower (HPT: reliability of 99.79%, 1.01x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.md)
- [📈time plot](bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.113x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base-mem.svg)
- [📄table](bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base.md)
- [📈time plot](bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34547459887)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787.json)

### vs. 3.12.6

- Geometric mean: 1.010x faster (HPT: reliability of 70.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.md)
- [📈time plot](bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 99.74%, 1.01x slower at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.md)
- [📈time plot](bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.120x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base-mem.svg)
- [📄table](bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base.md)
- [📈time plot](bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base.svg)

