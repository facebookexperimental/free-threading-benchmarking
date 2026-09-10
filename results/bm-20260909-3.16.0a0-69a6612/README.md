# Results

- fork: python/69a6612ff02c022d17f9
- version: 3.16.0a0
- config: 
- commit hash: [69a6612](https://github.com/python/cpython/commit/69a6612)
- commit date: 2026-09-09T17:08:37-07:00
- commit merge base: [939865532c00e25842209f56953abe0361ab22a1](https://github.com/python/cpython/commit/939865532c00e25842209f56953abe0361ab22a1)
- ref: 69a6612ff02c022d17f9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34422222550)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.md)
- [📈time plot](bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x faster (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.md)
- [📈time plot](bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34422222550)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612.json)

### vs. 3.12.6

- Geometric mean: 1.153x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.md)
- [📈time plot](bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.md)
- [📈time plot](bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.svg)

