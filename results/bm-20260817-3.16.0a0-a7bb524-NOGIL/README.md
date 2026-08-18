# Results

- fork: python/a7bb524fef61f77ede01
- version: 3.16.0a0
- config: NOGIL
- commit hash: [a7bb524](https://github.com/python/cpython/commit/a7bb524)
- commit date: 2026-08-17T22:39:16+03:00
- commit merge base: [b94b9c8886a987a324a677b5fda5bef27f15cb14](https://github.com/python/cpython/commit/b94b9c8886a987a324a677b5fda5bef27f15cb14)
- ref: a7bb524fef61f77ede01

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32083886482)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 91.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.md)
- [📈time plot](bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 99.62%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.md)
- [📈time plot](bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.110x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base-mem.svg)
- [📄table](bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base.md)
- [📈time plot](bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32083886482)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 63.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.md)
- [📈time plot](bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 99.67%, 1.01x slower at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.md)
- [📈time plot](bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base-mem.svg)
- [📄table](bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base.md)
- [📈time plot](bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base.svg)

