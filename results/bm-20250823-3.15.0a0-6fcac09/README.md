# Results

- fork: python/6fcac09401e336b25833
- version: 3.15.0a0
- config: 
- commit hash: [6fcac09](https://github.com/python/cpython/commit/6fcac09)
- commit date: 2025-08-23T15:18:46Z
- commit merge base: [ab1bef8ad27ad531a1109cfc016ea627d94f9cc1](https://github.com/python/cpython/commit/ab1bef8ad27ad531a1109cfc016ea627d94f9cc1)
- commit date: 2025-08-23T15:18:46+00:00
- ref: 6fcac09401e336b25833

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17181749269)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-pystats.json)
- [pystats table](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-pystats.md)
- [raw results](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.12.6.md)
- [📈time plot](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.13.0rc2.md)
- [📈time plot](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17181749269)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09.json)

### vs. 3.12.6

- Geometric mean: 1.117x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.12.6.md)
- [📈time plot](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 99.70%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.13.0rc2.md)
- [📈time plot](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.13.0rc2.svg)

