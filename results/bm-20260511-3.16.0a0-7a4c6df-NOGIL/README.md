# Results

- fork: python/7a4c6dfb8839eb05fb87
- version: 3.16.0a0
- config: NOGIL
- commit hash: [7a4c6df](https://github.com/python/cpython/commit/7a4c6df)
- commit date: 2026-05-11T18:20:09-04:00
- commit merge base: [8a4895985f42282504d83b9bd0c77b129f95a5d5](https://github.com/python/cpython/commit/8a4895985f42282504d83b9bd0c77b129f95a5d5)
- ref: 7a4c6dfb8839eb05fb87

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25706383170)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 92.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.md)
- [📈time plot](bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.md)
- [📈time plot](bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base-mem.svg)
- [📄table](bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base.md)
- [📈time plot](bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25706383170)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df.json)

### vs. 3.12.6

- Geometric mean: 1.115x faster (HPT: reliability of 99.93%, 1.02x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.md)
- [📈time plot](bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 65.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.md)
- [📈time plot](bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.041x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base-mem.svg)
- [📄table](bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base.md)
- [📈time plot](bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base.svg)

