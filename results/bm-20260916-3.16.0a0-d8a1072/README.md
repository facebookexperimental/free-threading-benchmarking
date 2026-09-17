# Results

- fork: python/d8a1072491069b825edc
- version: 3.16.0a0
- config: 
- commit hash: [d8a1072](https://github.com/python/cpython/commit/d8a1072)
- commit date: 2026-09-16T16:10:40-04:00
- commit merge base: [9cc3547536787ab8375c711ce56601c6b51f0461](https://github.com/python/cpython/commit/9cc3547536787ab8375c711ce56601c6b51f0461)
- ref: d8a1072491069b825edc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35167521043)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260916-vultr-x86_64-python-d8a1072491069b825edc-3.16.0a0-d8a1072.json)

### vs. 3.12.6

- Geometric mean: 1.064x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260916-vultr-x86_64-python-d8a1072491069b825edc-3.16.0a0-d8a1072-vs-3.12.6.md)
- [📈time plot](bm-20260916-vultr-x86_64-python-d8a1072491069b825edc-3.16.0a0-d8a1072-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 99.91%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260916-vultr-x86_64-python-d8a1072491069b825edc-3.16.0a0-d8a1072-vs-3.13.0rc2.md)
- [📈time plot](bm-20260916-vultr-x86_64-python-d8a1072491069b825edc-3.16.0a0-d8a1072-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35167521043)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260916-macm4pro-arm64-python-d8a1072491069b825edc-3.16.0a0-d8a1072.json)

### vs. 3.12.6

- Geometric mean: 1.141x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260916-macm4pro-arm64-python-d8a1072491069b825edc-3.16.0a0-d8a1072-vs-3.12.6.md)
- [📈time plot](bm-20260916-macm4pro-arm64-python-d8a1072491069b825edc-3.16.0a0-d8a1072-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 99.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260916-macm4pro-arm64-python-d8a1072491069b825edc-3.16.0a0-d8a1072-vs-3.13.0rc2.md)
- [📈time plot](bm-20260916-macm4pro-arm64-python-d8a1072491069b825edc-3.16.0a0-d8a1072-vs-3.13.0rc2.svg)

