# Results

- fork: python/5334732f9c8a44722e4b
- version: 3.15.0a0
- config: 
- commit hash: [5334732](https://github.com/python/cpython/commit/5334732)
- commit date: 2025-06-28T14:11:31+01:00
- commit merge base: [579acf45629fa0b7787ec78fa4049fc6a6388b71](https://github.com/python/cpython/commit/579acf45629fa0b7787ec78fa4049fc6a6388b71)
- ref: 5334732f9c8a44722e4b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15949559357)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-pystats.json)
- [pystats table](bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-pystats.md)
- [raw results](bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732.json)

### vs. 3.12.6

- Geometric mean: 1.112x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-vs-3.12.6.md)
- [📈time plot](bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-vs-3.13.0rc2.md)
- [📈time plot](bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15949559357)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250628-macm4pro-arm64-python-5334732f9c8a44722e4b-3.15.0a0-5334732.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250628-macm4pro-arm64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-vs-3.12.6.md)
- [📈time plot](bm-20250628-macm4pro-arm64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 69.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250628-macm4pro-arm64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-vs-3.13.0rc2.md)
- [📈time plot](bm-20250628-macm4pro-arm64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-vs-3.13.0rc2.svg)

