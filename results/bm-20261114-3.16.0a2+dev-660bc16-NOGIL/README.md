# Results

- fork: python/660bc166b46683578397
- version: 3.16.0a2+dev
- config: NOGIL
- commit hash: [660bc16](https://github.com/python/cpython/commit/660bc16)
- commit date: 2026-11-14T00:59:53+01:00
- commit merge base: [5151e7f2a3dabf74941f2c3857e17886d87cb5dd](https://github.com/python/cpython/commit/5151e7f2a3dabf74941f2c3857e17886d87cb5dd)
- ref: 660bc166b46683578397

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43533972423)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 76.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.12.6.md)
- [📈time plot](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x slower (HPT: reliability of 91.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.13.0rc2.md)
- [📈time plot](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-base-mem.svg)
- [📄table](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-base.md)
- [📈time plot](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43533972423)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 97.95%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.12.6.md)
- [📈time plot](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x slower (HPT: reliability of 83.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.13.0rc2.md)
- [📈time plot](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.07x
- new benchmarks: coverage
- [🧠memory plot](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-base-mem.svg)
- [📄table](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-base.md)
- [📈time plot](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-base.svg)

