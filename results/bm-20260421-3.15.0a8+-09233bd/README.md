# Results

- fork: python/09233bd19879284395af
- version: 3.15.0a8+
- config: 
- commit hash: [09233bd](https://github.com/python/cpython/commit/09233bd)
- commit date: 2026-04-21T12:49:44-07:00
- commit merge base: [0b9146e90b4969af8cd6ed39c3d97bb71bfc6a7a](https://github.com/python/cpython/commit/0b9146e90b4969af8cd6ed39c3d97bb71bfc6a7a)
- ref: 09233bd19879284395af

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24754118297)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd.json)

### vs. 3.12.6

- Geometric mean: 1.081x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.md)
- [📈time plot](bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.045x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.md)
- [📈time plot](bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24754118297)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd.json)

### vs. 3.12.6

- Geometric mean: 1.171x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.md)
- [📈time plot](bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.md)
- [📈time plot](bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.svg)

