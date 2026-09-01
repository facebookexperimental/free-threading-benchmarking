# Results

- fork: python/b38e073f1be8fe40af99
- version: 3.16.0a0
- config: NOGIL
- commit hash: [b38e073](https://github.com/python/cpython/commit/b38e073)
- commit date: 2026-08-31T14:54:35-07:00
- commit merge base: [c83013c92dfdc77b87a523b736b76d5abb8ede2a](https://github.com/python/cpython/commit/c83013c92dfdc77b87a523b736b76d5abb8ede2a)
- ref: b38e073f1be8fe40af99

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33456317460)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260831-vultr-x86_64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 80.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260831-vultr-x86_64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-3.12.6.md)
- [📈time plot](bm-20260831-vultr-x86_64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 96.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260831-vultr-x86_64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-3.13.0rc2.md)
- [📈time plot](bm-20260831-vultr-x86_64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260831-vultr-x86_64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-base-mem.svg)
- [📄table](bm-20260831-vultr-x86_64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-base.md)
- [📈time plot](bm-20260831-vultr-x86_64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33456317460)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073.json)

### vs. 3.12.6

- Geometric mean: 1.013x faster (HPT: reliability of 68.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-3.12.6.md)
- [📈time plot](bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 99.82%, 1.01x slower at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-3.13.0rc2.md)
- [📈time plot](bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-base-mem.svg)
- [📄table](bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-base.md)
- [📈time plot](bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073-vs-base.svg)

