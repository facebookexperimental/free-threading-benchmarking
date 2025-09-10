# Results

- fork: python/766e7f150ae93d637824
- version: 3.15.0a0
- config: NOGIL
- commit hash: [766e7f1](https://github.com/python/cpython/commit/766e7f1)
- commit date: 2025-09-10T00:08:09Z
- commit merge base: [137519a38ccabcb009a2b1b7eab1fbbf9c3ceae0](https://github.com/python/cpython/commit/137519a38ccabcb009a2b1b7eab1fbbf9c3ceae0)
- commit date: 2025-09-10T00:08:09+00:00
- ref: 766e7f150ae93d637824

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17599259705)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 94.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.md)
- [📈time plot](bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 98.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base-mem.svg)
- [📄table](bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base.md)
- [📈time plot](bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17599259705)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 94.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.md)
- [📈time plot](bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 71.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 99.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base-mem.svg)
- [📄table](bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base.md)
- [📈time plot](bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base.svg)

