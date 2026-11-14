# Results

- fork: python/660bc166b46683578397
- version: 3.16.0a2+dev
- config: 
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

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.12.6.md)
- [📈time plot](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 99.84%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.13.0rc2.md)
- [📈time plot](bm-20261114-vultr-x86_64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43533972423)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16.json)

### vs. 3.12.6

- Geometric mean: 1.201x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.12.6.md)
- [📈time plot](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.13.0rc2.md)
- [📈time plot](bm-20261114-macm4pro-arm64-python-660bc166b46683578397-3.16.0a2%2Bdev-660bc16-vs-3.13.0rc2.svg)

