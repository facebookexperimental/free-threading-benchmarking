# Results

- fork: python/7b4364de251265b7920a
- version: 3.16.0a0
- config: NOGIL
- commit hash: [7b4364d](https://github.com/python/cpython/commit/7b4364d)
- commit date: 2026-09-03T15:20:52-07:00
- commit merge base: [0625799652a4876171103e985057ee3546441d95](https://github.com/python/cpython/commit/0625799652a4876171103e985057ee3546441d95)
- ref: 7b4364de251265b7920a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33822659729)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260903-vultr-x86_64-python-7b4364de251265b7920a-3.16.0a0-7b4364d.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 88.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260903-vultr-x86_64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-3.12.6.md)
- [📈time plot](bm-20260903-vultr-x86_64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 97.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260903-vultr-x86_64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260903-vultr-x86_64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260903-vultr-x86_64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-base-mem.svg)
- [📄table](bm-20260903-vultr-x86_64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-base.md)
- [📈time plot](bm-20260903-vultr-x86_64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33822659729)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260903-macm4pro-arm64-python-7b4364de251265b7920a-3.16.0a0-7b4364d.json)

### vs. 3.12.6

- Geometric mean: 1.006x faster (HPT: reliability of 75.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260903-macm4pro-arm64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-3.12.6.md)
- [📈time plot](bm-20260903-macm4pro-arm64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 99.85%, 1.02x slower at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260903-macm4pro-arm64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260903-macm4pro-arm64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.122x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260903-macm4pro-arm64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-base-mem.svg)
- [📄table](bm-20260903-macm4pro-arm64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-base.md)
- [📈time plot](bm-20260903-macm4pro-arm64-python-7b4364de251265b7920a-3.16.0a0-7b4364d-vs-base.svg)

