# Results

- fork: python/e3287f631f3c88ed8019
- version: 3.16.0a0
- config: NOGIL
- commit hash: [e3287f6](https://github.com/python/cpython/commit/e3287f6)
- commit date: 2026-08-15T20:47:06Z
- commit merge base: [1a52eaedce6f1d32cdb5ee18ecec74cfd82d5550](https://github.com/python/cpython/commit/1a52eaedce6f1d32cdb5ee18ecec74cfd82d5550)
- commit date: 2026-08-15T20:47:06+00:00
- ref: e3287f631f3c88ed8019

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31916518490)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 84.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)
- [📈time plot](bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 96.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)
- [📈time plot](bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base-mem.svg)
- [📄table](bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.md)
- [📈time plot](bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31916518490)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6.json)

### vs. 3.12.6

- Geometric mean: 1.017x faster (HPT: reliability of 70.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)
- [📈time plot](bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 99.71%, 1.01x slower at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)
- [📈time plot](bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base-mem.svg)
- [📄table](bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.md)
- [📈time plot](bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.svg)

