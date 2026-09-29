# Results

- fork: python/333071231d3a46cccc32
- version: 3.16.0a0
- config: NOGIL
- commit hash: [3330712](https://github.com/python/cpython/commit/3330712)
- commit date: 2026-09-28T19:18:28Z
- commit merge base: [6e32490d922cc0b9376f06da0325e79fb6fb8ef8](https://github.com/python/cpython/commit/6e32490d922cc0b9376f06da0325e79fb6fb8ef8)
- commit date: 2026-09-28T19:18:28+00:00
- ref: 333071231d3a46cccc32

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36504546792)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 91.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.md)
- [📈time plot](bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 98.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.md)
- [📈time plot](bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base-mem.svg)
- [📄table](bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base.md)
- [📈time plot](bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36504546792)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712.json)

### vs. 3.12.6

- Geometric mean: 1.002x slower (HPT: reliability of 86.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.md)
- [📈time plot](bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.88%, 1.03x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.md)
- [📈time plot](bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.122x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base-mem.svg)
- [📄table](bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base.md)
- [📈time plot](bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base.svg)

