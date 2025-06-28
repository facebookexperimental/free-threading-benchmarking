# Results

- fork: python/c419af9e277bea7dd78f
- version: 3.15.0a0
- config: NOGIL
- commit hash: [c419af9](https://github.com/python/cpython/commit/c419af9)
- commit date: 2025-06-28T00:18:44+08:00
- commit merge base: [0e5d09613094f2331a6b1cdb83f98998702d4469](https://github.com/python/cpython/commit/0e5d09613094f2331a6b1cdb83f98998702d4469)
- ref: c419af9e277bea7dd78f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15938416389)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json)

### vs. 3.12.6

- Geometric mean: 1.023x faster (HPT: reliability of 85.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.md)
- [📈time plot](bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x slower (HPT: reliability of 94.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base-mem.svg)
- [📄table](bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base.md)
- [📈time plot](bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15938416389)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 97.06%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.md)
- [📈time plot](bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 73.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 86.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base-mem.svg)
- [📄table](bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base.md)
- [📈time plot](bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base.svg)

