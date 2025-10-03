# Results

- fork: python/4e7e2dd043c1da85b0c1
- version: 3.15.0a0
- config: 
- commit hash: [4e7e2dd](https://github.com/python/cpython/commit/4e7e2dd)
- commit date: 2025-10-02T20:51:57Z
- commit merge base: [fb114cf49742a3679d56aa4ac3f341839c641221](https://github.com/python/cpython/commit/fb114cf49742a3679d56aa4ac3f341839c641221)
- commit date: 2025-10-02T20:51:57+00:00
- ref: 4e7e2dd043c1da85b0c1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18209203936)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.md)
- [📈time plot](bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.md)
- [📈time plot](bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18209203936)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.md)
- [📈time plot](bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x faster (HPT: reliability of 61.39%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.md)
- [📈time plot](bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.svg)

