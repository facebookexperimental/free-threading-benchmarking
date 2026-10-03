# Results

- fork: python/1a85213940896f180cbc
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1a85213](https://github.com/python/cpython/commit/1a85213)
- commit date: 2026-10-03T00:34:38+02:00
- commit merge base: [b4197da019f4a77a649a17e0b9c4ddf7c137229c](https://github.com/python/cpython/commit/b4197da019f4a77a649a17e0b9c4ddf7c137229c)
- ref: 1a85213940896f180cbc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37083099470)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261003-vultr-x86_64-python-1a85213940896f180cbc-3.16.0a0-1a85213.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 86.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261003-vultr-x86_64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-3.12.6.md)
- [📈time plot](bm-20261003-vultr-x86_64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x slower (HPT: reliability of 98.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261003-vultr-x86_64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-3.13.0rc2.md)
- [📈time plot](bm-20261003-vultr-x86_64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261003-vultr-x86_64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-base-mem.svg)
- [📄table](bm-20261003-vultr-x86_64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-base.md)
- [📈time plot](bm-20261003-vultr-x86_64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37083099470)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261003-macm4pro-arm64-python-1a85213940896f180cbc-3.16.0a0-1a85213.json)

### vs. 3.12.6

- Geometric mean: 1.056x faster (HPT: reliability of 84.34%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261003-macm4pro-arm64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-3.12.6.md)
- [📈time plot](bm-20261003-macm4pro-arm64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x slower (HPT: reliability of 96.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261003-macm4pro-arm64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-3.13.0rc2.md)
- [📈time plot](bm-20261003-macm4pro-arm64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261003-macm4pro-arm64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-base-mem.svg)
- [📄table](bm-20261003-macm4pro-arm64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-base.md)
- [📈time plot](bm-20261003-macm4pro-arm64-python-1a85213940896f180cbc-3.16.0a0-1a85213-vs-base.svg)

