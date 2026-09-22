# Results

- fork: python/212e6035133957a66f1a
- version: 3.16.0a0
- config: NOGIL
- commit hash: [212e603](https://github.com/python/cpython/commit/212e603)
- commit date: 2026-09-21T17:00:06-04:00
- commit merge base: [02fae7a9594953c1d8b298b08d6faa99a5c18975](https://github.com/python/cpython/commit/02fae7a9594953c1d8b298b08d6faa99a5c18975)
- ref: 212e6035133957a66f1a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35672970556)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 90.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.md)
- [📈time plot](bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 98.94%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.md)
- [📈time plot](bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base-mem.svg)
- [📄table](bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base.md)
- [📈time plot](bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35672970556)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603.json)

### vs. 3.12.6

- Geometric mean: 1.002x faster (HPT: reliability of 86.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.md)
- [📈time plot](bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.82%, 1.02x slower at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.md)
- [📈time plot](bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.119x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base-mem.svg)
- [📄table](bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base.md)
- [📈time plot](bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base.svg)

