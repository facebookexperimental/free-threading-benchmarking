# Results

- fork: python/800d37feca2e0ea33439
- version: 3.15.0a0
- config: 
- commit hash: [800d37f](https://github.com/python/cpython/commit/800d37f)
- commit date: 2025-07-19T21:43:50+02:00
- commit merge base: [69ea1b3a8f45fec46add3272ad47f14ff5321ae8](https://github.com/python/cpython/commit/69ea1b3a8f45fec46add3272ad47f14ff5321ae8)
- ref: 800d37feca2e0ea33439

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16394127171)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-pystats.json)
- [pystats table](bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-pystats.md)
- [raw results](bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-vs-3.12.6.md)
- [📈time plot](bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.041x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16394127171)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-vs-3.12.6.md)
- [📈time plot](bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 76.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-vs-3.13.0rc2.svg)

