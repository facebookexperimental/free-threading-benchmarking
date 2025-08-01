# Results

- fork: python/9312702d2e12c2f58f02
- version: 3.15.0a0
- config: NOGIL
- commit hash: [9312702](https://github.com/python/cpython/commit/9312702)
- commit date: 2025-07-06T16:44:20-07:00
- commit merge base: [c89f76e6c4ca9b0200d5cc8cf0a675a76de50ba8](https://github.com/python/cpython/commit/c89f76e6c4ca9b0200d5cc8cf0a675a76de50ba8)
- ref: 9312702d2e12c2f58f02

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16104841710)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250706-vultr-x86_64-python-9312702d2e12c2f58f02-3.15.0a0-9312702.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 93.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250706-vultr-x86_64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-3.12.6.md)
- [📈time plot](bm-20250706-vultr-x86_64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 97.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250706-vultr-x86_64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-3.13.0rc2.md)
- [📈time plot](bm-20250706-vultr-x86_64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250706-vultr-x86_64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-base-mem.svg)
- [📄table](bm-20250706-vultr-x86_64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-base.md)
- [📈time plot](bm-20250706-vultr-x86_64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16104841710)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250706-macm4pro-arm64-python-9312702d2e12c2f58f02-3.15.0a0-9312702.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 98.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250706-macm4pro-arm64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-3.12.6.md)
- [📈time plot](bm-20250706-macm4pro-arm64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 57.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250706-macm4pro-arm64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-3.13.0rc2.md)
- [📈time plot](bm-20250706-macm4pro-arm64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 86.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250706-macm4pro-arm64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-base-mem.svg)
- [📄table](bm-20250706-macm4pro-arm64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-base.md)
- [📈time plot](bm-20250706-macm4pro-arm64-python-9312702d2e12c2f58f02-3.15.0a0-9312702-vs-base.svg)

