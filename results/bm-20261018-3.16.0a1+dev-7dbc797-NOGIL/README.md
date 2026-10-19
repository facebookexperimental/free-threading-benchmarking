# Results

- fork: python/7dbc7975db8e34db8be8
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [7dbc797](https://github.com/python/cpython/commit/7dbc797)
- commit date: 2026-10-18T21:55:24+05:30
- commit merge base: [0f2eb5a36280fc88cb031ebaa441e5b717660eb8](https://github.com/python/cpython/commit/0f2eb5a36280fc88cb031ebaa441e5b717660eb8)
- ref: 7dbc7975db8e34db8be8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39181915226)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797.json)

### vs. 3.12.6

- Geometric mean: 1.045x slower (HPT: reliability of 86.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-3.12.6.md)
- [📈time plot](bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-3.13.0rc2.md)
- [📈time plot](bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.116x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-base-mem.svg)
- [📄table](bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-base.md)
- [📈time plot](bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39181915226)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 95.45%, 1.00x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-3.12.6.md)
- [📈time plot](bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 78.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-3.13.0rc2.md)
- [📈time plot](bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-base-mem.svg)
- [📄table](bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-base.md)
- [📈time plot](bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1%2Bdev-7dbc797-vs-base.svg)

