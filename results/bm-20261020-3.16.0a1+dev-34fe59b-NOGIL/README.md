# Results

- fork: python/34fe59b878335856ddfe
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [34fe59b](https://github.com/python/cpython/commit/34fe59b)
- commit date: 2026-10-20T02:32:08+02:00
- commit merge base: [fa8600cb1dd2ad33e95d3cfbed55208e35f5b472](https://github.com/python/cpython/commit/fa8600cb1dd2ad33e95d3cfbed55208e35f5b472)
- ref: 34fe59b878335856ddfe

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39348925828)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261020-vultr-x86_64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 70.55%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.12.6.md)
- [📈time plot](bm-20261020-vultr-x86_64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 94.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261020-vultr-x86_64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.112x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261020-vultr-x86_64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-base-mem.svg)
- [📄table](bm-20261020-vultr-x86_64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-base.md)
- [📈time plot](bm-20261020-vultr-x86_64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39348925828)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 95.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.12.6.md)
- [📈time plot](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x slower (HPT: reliability of 79.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-base-mem.svg)
- [📄table](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-base.md)
- [📈time plot](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-base.svg)

