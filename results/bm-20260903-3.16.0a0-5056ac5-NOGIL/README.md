# Results

- fork: python/5056ac552a413b394fd1
- version: 3.16.0a0
- config: NOGIL
- commit hash: [5056ac5](https://github.com/python/cpython/commit/5056ac5)
- commit date: 2026-09-03T00:10:23+03:00
- commit merge base: [d16a691111503798820a4b3a60ffae7b76c4d85a](https://github.com/python/cpython/commit/d16a691111503798820a4b3a60ffae7b76c4d85a)
- ref: 5056ac552a413b394fd1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33700644519)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260903-vultr-x86_64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 86.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260903-vultr-x86_64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-3.12.6.md)
- [📈time plot](bm-20260903-vultr-x86_64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 98.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260903-vultr-x86_64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260903-vultr-x86_64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260903-vultr-x86_64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-base-mem.svg)
- [📄table](bm-20260903-vultr-x86_64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-base.md)
- [📈time plot](bm-20260903-vultr-x86_64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33700644519)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260903-macm4pro-arm64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5.json)

### vs. 3.12.6

- Geometric mean: 1.008x faster (HPT: reliability of 79.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260903-macm4pro-arm64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-3.12.6.md)
- [📈time plot](bm-20260903-macm4pro-arm64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 99.85%, 1.01x slower at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260903-macm4pro-arm64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260903-macm4pro-arm64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.119x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20260903-macm4pro-arm64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-base-mem.svg)
- [📄table](bm-20260903-macm4pro-arm64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-base.md)
- [📈time plot](bm-20260903-macm4pro-arm64-python-5056ac552a413b394fd1-3.16.0a0-5056ac5-vs-base.svg)

